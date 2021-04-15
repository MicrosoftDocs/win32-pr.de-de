---
description: In diesem Beispiel wird veranschaulicht, wie frei Hand Eingaben in verschiedenen Formaten serialisiert und deserialisiert werden.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Beispiel für eine Ink-Serialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e898f91db17efcb7579c067e7db5c422da8213a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525289"
---
# <a name="ink-serialization-sample"></a>Beispiel für eine Ink-Serialisierung

In diesem Beispiel wird veranschaulicht, wie frei Hand Eingaben in verschiedenen Formaten serialisiert und deserialisiert werden. Die Anwendung stellt ein Formular mit Feldern zum Einfügen von Vorname, Nachname und Signatur dar. Der Benutzer kann diese Daten als reines frei Hand Format (Ink serialisiert Format, ISF), Extensible Markup Language (XML) mithilfe von Base64-codiertem ISF oder HTML speichern, das auf Ink in einem GIF-Image (Base64-codiertes GIF Graphics Interchange Format) verweist. Die Anwendung ermöglicht dem Benutzer auch das Öffnen von Dateien, die als XML-und ISF-Formate gespeichert wurden. Das ISF-Format verwendet erweiterte Eigenschaften, um den Vornamen und den Nachnamen zu speichern, während die XML-und HTML-Formate diese Informationen in benutzerdefinierten Attributen speichern.

Dieses Beispiel unterstützt das Laden aus dem HTML-Format nicht, da HTML nicht zum Speichern strukturierter Daten geeignet ist. Da die Daten in Name, Signatur usw. unterteilt sind, ist ein Format erforderlich, das diese Trennung beibehält, z. b. XML oder eine andere Art von Datenbankformat.

HTML ist sehr nützlich in einer Umgebung, in der die Formatierung wichtig ist, z. b. in einem Textverarbeitungsdokument. Der HTML-Code, der in diesem Beispiel gespeichert wird, verwendet befestigte GIFs. Diese GIFs verfügen über ISF, das in Sie eingebettet ist und die vollständige Treue der frei Hand Eingaben beibehält. Eine Textverarbeitungsanwendung kann ein Dokument speichern, das mehrere Datentypen enthält, z. b. Bilder, Tabellen, formatierten Text und frei Hand Eingaben, die in einem HTML-Format beibehalten werden. Dieser HTML-Code wird in Browsern angezeigt, die keine frei Hand Eingaben erkennen. Beim Laden in eine Anwendung, für die frei Hand Eingaben aktiviert ist, ist die vollständige Genauigkeit der ursprünglichen frei Hand Eingaben jedoch verfügbar und kann gerendert, bearbeitet oder zur Erkennung verwendet werden.

In diesem Beispiel werden die folgenden Funktionen verwendet:

-   Die [Load](/previous-versions/ms569609(v=vs.100)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts
-   Die [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts.
-   Die [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) -Eigenschaft des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts

## <a name="collecting-ink"></a>Erfassen von Freihandeingaben

Verweisen Sie zunächst auf die Tablet PC-API, die mit Windows Vista und Windows XP Tablet PC Edition Software Development Kit (SDK) installiert wird.


```C++
using Microsoft.Ink;
```



Der-Konstruktor erstellt und aktiviert einen [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , für das Formular.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Speichern einer Datei

Die- `SaveAsMenu_Click` Methode behandelt das Dialogfeld Speichern unter, erstellt einen Dateistream, in dem die frei Hand Daten gespeichert werden, und ruft die Save-Methode auf, die der Auswahl des Benutzers entspricht.

## <a name="saving-to-an-isf-file"></a>Speichern in einer ISF-Datei

In der `SaveISF` -Methode werden die Werte für den vor-und Nachnamen der [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) -Eigenschaft der [Ink](/previous-versions/ms836505(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekts hinzugefügt, bevor die frei Hand Eingaben serialisiert und in die Datei geschrieben werden. Nachdem die frei Hand Eingaben serialisiert wurden, werden die Werte für den Vornamen und den Nachnamen aus der ExtendedProperties-Eigenschaft des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts entfernt.


```C++
byte[] isf;

// This is the ink object which is serialized
ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Store the name fields in the ink object
// These fields roundtrip through the ISF format
// Ignore empty fields since strictly empty strings 
//       cannot be stored in ExtendedProperties.
if (FirstNameBox.Text.Length > 0)
{
    inkProperties.Add(FirstName, FirstNameBox.Text);
}
if (LastNameBox.Text.Length > 0)
{
    inkProperties.Add(LastName, LastNameBox.Text);
}

// Perform the serialization
isf = ic.Ink.Save(PersistenceFormat.InkSerializedFormat);

// If the first and last names were added as extended
// properties to the ink, remove them - these properties
// are only used for the save and there is no need to
// keep them around on the ink object.
if (inkProperties.DoesPropertyExist(FirstName))
{
    inkProperties.Remove(FirstName);
}
if (inkProperties.DoesPropertyExist(LastName))
{
    inkProperties.Remove(LastName);
}

// Write the ISF to the stream
s.Write(isf,0,isf.Length);
```



## <a name="saving-to-an-xml-file"></a>Speichern in einer XML-Datei

In der- `SaveXML` Methode wird ein [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) -Objekt verwendet, um ein XML-Dokument zu erstellen und in dieses zu schreiben. Mithilfe der [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts wird die frei Hand Eingabe in ein Base64-codiertes, serialisiertes frei Hand Format-Bytearray konvertiert. Anschließend wird das Bytearray in eine Zeichenfolge konvertiert, die in die XML-Datei geschrieben werden soll. Die Textdaten aus dem Formular werden auch in die XML-Datei geschrieben.


```C++
// Get the base64 encoded ISF
base64ISF_bytes = ic.Ink.Save(PersistenceFormat.Base64InkSerializedFormat);

// Convert it to a String
base64ISF_string = utf8.GetString(base64ISF_bytes);

// Write the ISF containing node to the XML
xwriter.WriteElementString("Ink", base64ISF_string);

// Write the text data from the form
// Note that the names are stored as XML fields, rather
// than custom properties, so that these properties can 
// be most easily accessible if the XML is saved in a database.
xwriter.WriteElementString("FirstName",FirstNameBox.Text);
xwriter.WriteElementString("LastName",LastNameBox.Text);
```



## <a name="saving-to-an-html-file"></a>Speichern in einer HTML-Datei

Die SaveHtml-Methode verwendet das umgebende Feld der [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung, um zu testen, ob eine Signatur vorhanden ist. Wenn die Signatur vorhanden ist, wird Sie mithilfe der [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode des Ink-Objekts in das befestigte GIF-Format konvertiert und in eine Datei geschrieben. Auf das GIF wird dann in der HTML-Datei verwiesen.


```C++
if (ic.Ink.Strokes.GetBoundingBox().IsEmpty)
{
   MessageBox.Show("Unable to save empty ink in HTML persistence format.");
}
else
{
    FileStream gifFile;
    byte[] fortifiedGif = null;
    ...

    // Create a directory to store the fortified GIF which also contains ISF
    // and open the file for writing
    Directory.CreateDirectory(nameBase + "_files");
    using (FileStream gifFile = File.OpenWrite(nameBase + "_files\\signature.gif"))
    {

        // Generate the fortified GIF represenation of the ink
        fortifiedGif = ic.Ink.Save(PersistenceFormat.Gif);

        // Write and close the gif file
        gifFile.Write(fortifiedGif, 0, fortifiedGif.Length);
    }
```



## <a name="loading-a-file"></a>Laden einer Datei

Die- `OpenMenu_Click` Methode behandelt das Dialogfeld öffnen, öffnet die Datei und ruft die Lademethode auf, die der Auswahl des Benutzers entspricht.

## <a name="loading-an-isf-file"></a>Laden einer ISF-Datei

Die `LoadISF` -Methode liest die zuvor erstellte Datei und konvertiert das Bytearray mit der [Load](/previous-versions/ms569609(v=vs.100)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts in frei Hand Eingaben. Der Ink Collector wird vorübergehend deaktiviert, um ihm das Ink-Objekt zuzuweisen. Die `LoadISF` Methode überprüft dann die [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) -Eigenschaft des Ink-Objekts für die vor-und Nachnamen-Zeichen folgen.


```C++
Ink loadedInk = new Ink();
byte[] isfBytes = new byte[s.Length];

// read in the ISF
s.Read(isfBytes, 0, (int) s.Length);

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
loadedInk.Load(isfBytes);

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Get the raw data out of this stroke's extended
// properties list, using the previously defined 
// Guid as a key to the extended property.
// Since the save method stored the first and last
// name information as extended properties, this
// information can be remove now that the load is complete.
if (inkProperties.DoesPropertyExist(FirstName))
{
    FirstNameBox.Text = (String) inkProperties[FirstName].Data;
    inkProperties.Remove(FirstName);
}
else
{
    FirstNameBox.Text = String.Empty;
}

if (inkProperties.DoesPropertyExist(LastName))
{
    LastNameBox.Text = (String) inkProperties[LastName].Data;
    inkProperties.Remove(LastName);
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="loading-an-xml-file"></a>Laden einer XML-Datei

Die `LoadXML` -Methode lädt eine zuvor erstellte XML-Datei, ruft Daten aus dem Ink-Knoten ab und konvertiert die Daten im Knoten mithilfe der [Load](/previous-versions/ms569609(v=vs.100)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts in Ink. Der [InkCollector](/previous-versions/ms836493(v=msdn.10)) wird vorübergehend deaktiviert, um ihm das Ink-Objekt zuzuweisen. Das Signatur Feld wird für ungültig erklärt, und die vor-und Nachnamen-Informationen werden aus dem XML-Dokument abgerufen.


```C++
// This object encodes our byte data to a UTF8 string
UTF8Encoding utf8 = new UTF8Encoding();

XmlDocument xd = new XmlDocument();
XmlNodeList nodes;
Ink loadedInk = new Ink();

// Load the XML data into a DOM
xd.Load(s);

// Get the data in the ink node
nodes = xd.GetElementsByTagName("Ink");

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
if (0 != nodes.Count)
    loadedInk.Load(utf8.GetBytes(nodes[0].InnerXml));

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

// Get the data in the FirstName node
nodes = xd.GetElementsByTagName("FirstName");
if (0 != nodes.Count)
{
    FirstNameBox.Text = nodes[0].InnerXml;
}
else
{
    FirstNameBox.Text = String.Empty;
}

// Get the data in the LastName node
nodes = xd.GetElementsByTagName("LastName");
if (0 != nodes.Count)
{
    LastNameBox.Text = nodes[0].InnerXml;
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="closing-the-form"></a>Schließen des Formulars

Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei.

 

 
