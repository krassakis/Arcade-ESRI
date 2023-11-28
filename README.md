# Arcade-ESRI
Arcade code for earthquake services

var event = $feature.mag;
var depth = $feature.depth;
var eventTime = Date($feature.updated); // Ensure this is a compatible date format

// Define your time threshold (e.g., 24 hours ago)
var timeThreshold = DateAdd(Now(), -24, 'hours');

if (event > 4 && depth < 15 && eventTime > timeThreshold) {
    return "Warning: Recent event within Greece's boundary with magnitude higher than 4 and depth less than 15";
} else {
    return "No Warning";
}

Με το var ορίζουμε τις μεταβλητές μας.
Event είναι το μέγεθος του σεισμού το οποίο το τραβάμε από τη στήλη mag ($feature.mag).
Depth είναι το βάθος του σεισμού.
EventTime είναι η ώρα του σεισμού.
Το timeThreshold είναι μια νέα μεταβλητή στην οποία λαμβάνει τη διαφορά μεταξύ του live χρόνου και του σεισμικού γεγονότος σε ένα διάστημα 24 ωρών.
Η πρόταση του if ορίζει την δημιουργία ενός αποτελέσματος που λειτουργεί ως warning system οπτικοποιώντας με διαφορετικό χρώμα τα σεισμικά γεγονότα τα οποία είναι εντός του τελευταίου 24ώρου με βάθος μικρότερο 15 km και μέγεθος μεγαλύτερο 4 Mw. 
  
Το αυτόματο αποτέλεσμα μας βγάζει τα χρώματα με τρόπο όπου μας μπερδεύσει επομένως μετα μπορούμε να αλλάξουμε τα χρώματα χειροκίνητα.


