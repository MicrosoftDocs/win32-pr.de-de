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
# <a name="ink-serialization-sample"></a><span data-ttu-id="786ff-103">Beispiel für eine Ink-Serialisierung</span><span class="sxs-lookup"><span data-stu-id="786ff-103">Ink Serialization Sample</span></span>

<span data-ttu-id="786ff-104">In diesem Beispiel wird veranschaulicht, wie frei Hand Eingaben in verschiedenen Formaten serialisiert und deserialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="786ff-104">This sample demonstrates how to serialize and de-serialize ink in various formats.</span></span> <span data-ttu-id="786ff-105">Die Anwendung stellt ein Formular mit Feldern zum Einfügen von Vorname, Nachname und Signatur dar.</span><span class="sxs-lookup"><span data-stu-id="786ff-105">The application represents a form with fields for inputting first name, last name, and signature.</span></span> <span data-ttu-id="786ff-106">Der Benutzer kann diese Daten als reines frei Hand Format (Ink serialisiert Format, ISF), Extensible Markup Language (XML) mithilfe von Base64-codiertem ISF oder HTML speichern, das auf Ink in einem GIF-Image (Base64-codiertes GIF Graphics Interchange Format) verweist.</span><span class="sxs-lookup"><span data-stu-id="786ff-106">The user may save this data as pure ink serialized format (ISF), Extensible Markup Language (XML) using base64 encoded ISF, or HTML, which references ink in a base64 encoded fortified Graphics Interchange Format (GIF) image.</span></span> <span data-ttu-id="786ff-107">Die Anwendung ermöglicht dem Benutzer auch das Öffnen von Dateien, die als XML-und ISF-Formate gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="786ff-107">The application also enables the user to open files that were saved as XML and ISF formats.</span></span> <span data-ttu-id="786ff-108">Das ISF-Format verwendet erweiterte Eigenschaften, um den Vornamen und den Nachnamen zu speichern, während die XML-und HTML-Formate diese Informationen in benutzerdefinierten Attributen speichern.</span><span class="sxs-lookup"><span data-stu-id="786ff-108">The ISF format uses extended properties to store the first name and last name, whereas the XML and HTML formats store this information in custom attributes.</span></span>

<span data-ttu-id="786ff-109">Dieses Beispiel unterstützt das Laden aus dem HTML-Format nicht, da HTML nicht zum Speichern strukturierter Daten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="786ff-109">This sample does not support loading from the HTML format, because HTML is not suitable for storing structured data.</span></span> <span data-ttu-id="786ff-110">Da die Daten in Name, Signatur usw. unterteilt sind, ist ein Format erforderlich, das diese Trennung beibehält, z. b. XML oder eine andere Art von Datenbankformat.</span><span class="sxs-lookup"><span data-stu-id="786ff-110">Because the data is separated into name, signature, and so on, a format that preserves this separation, such as XML or another kind of database format, is required.</span></span>

<span data-ttu-id="786ff-111">HTML ist sehr nützlich in einer Umgebung, in der die Formatierung wichtig ist, z. b. in einem Textverarbeitungsdokument.</span><span class="sxs-lookup"><span data-stu-id="786ff-111">HTML is very useful in an environment in which formatting is important, such as in a word processing document.</span></span> <span data-ttu-id="786ff-112">Der HTML-Code, der in diesem Beispiel gespeichert wird, verwendet befestigte GIFs.</span><span class="sxs-lookup"><span data-stu-id="786ff-112">The HTML that is saved by this sample uses fortified GIFs.</span></span> <span data-ttu-id="786ff-113">Diese GIFs verfügen über ISF, das in Sie eingebettet ist und die vollständige Treue der frei Hand Eingaben beibehält.</span><span class="sxs-lookup"><span data-stu-id="786ff-113">These GIFs have ISF embedded within them, which preserves the full fidelity of the ink.</span></span> <span data-ttu-id="786ff-114">Eine Textverarbeitungsanwendung kann ein Dokument speichern, das mehrere Datentypen enthält, z. b. Bilder, Tabellen, formatierten Text und frei Hand Eingaben, die in einem HTML-Format beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="786ff-114">A word processing application can save a document containing multiple types of data, such as images, tables, formatted text, and ink persisted in an HTML format.</span></span> <span data-ttu-id="786ff-115">Dieser HTML-Code wird in Browsern angezeigt, die keine frei Hand Eingaben erkennen.</span><span class="sxs-lookup"><span data-stu-id="786ff-115">This HTML would render in browsers that do not recognize ink.</span></span> <span data-ttu-id="786ff-116">Beim Laden in eine Anwendung, für die frei Hand Eingaben aktiviert ist, ist die vollständige Genauigkeit der ursprünglichen frei Hand Eingaben jedoch verfügbar und kann gerendert, bearbeitet oder zur Erkennung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="786ff-116">However, when loaded into an application that is ink-enabled, the full fidelity of the original ink is available and can be rendered, edited, or used for recognition.</span></span>

<span data-ttu-id="786ff-117">In diesem Beispiel werden die folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="786ff-117">The following features are used in this sample:</span></span>

-   <span data-ttu-id="786ff-118">Die [Load](/previous-versions/ms569609(v=vs.100)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts</span><span class="sxs-lookup"><span data-stu-id="786ff-118">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method</span></span>
-   <span data-ttu-id="786ff-119">Die [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="786ff-119">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method</span></span>
-   <span data-ttu-id="786ff-120">Die [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) -Eigenschaft des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts</span><span class="sxs-lookup"><span data-stu-id="786ff-120">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property</span></span>

## <a name="collecting-ink"></a><span data-ttu-id="786ff-121">Erfassen von Freihandeingaben</span><span class="sxs-lookup"><span data-stu-id="786ff-121">Collecting Ink</span></span>

<span data-ttu-id="786ff-122">Verweisen Sie zunächst auf die Tablet PC-API, die mit Windows Vista und Windows XP Tablet PC Edition Software Development Kit (SDK) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="786ff-122">First, reference the Tablet PC API, which are installed with the Windows Vista and Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="786ff-123">Der-Konstruktor erstellt und aktiviert einen [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , für das Formular.</span><span class="sxs-lookup"><span data-stu-id="786ff-123">The constructor creates and enables an [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic`, for the form.</span></span>


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a><span data-ttu-id="786ff-124">Speichern einer Datei</span><span class="sxs-lookup"><span data-stu-id="786ff-124">Saving a File</span></span>

<span data-ttu-id="786ff-125">Die- `SaveAsMenu_Click` Methode behandelt das Dialogfeld Speichern unter, erstellt einen Dateistream, in dem die frei Hand Daten gespeichert werden, und ruft die Save-Methode auf, die der Auswahl des Benutzers entspricht.</span><span class="sxs-lookup"><span data-stu-id="786ff-125">The `SaveAsMenu_Click` method handles the Save As dialog box, creates a file stream in which to save the ink data, and calls the save method that corresponds to the user's choice.</span></span>

## <a name="saving-to-an-isf-file"></a><span data-ttu-id="786ff-126">Speichern in einer ISF-Datei</span><span class="sxs-lookup"><span data-stu-id="786ff-126">Saving to an ISF File</span></span>

<span data-ttu-id="786ff-127">In der `SaveISF` -Methode werden die Werte für den vor-und Nachnamen der [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) -Eigenschaft der [Ink](/previous-versions/ms836505(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekts hinzugefügt, bevor die frei Hand Eingaben serialisiert und in die Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="786ff-127">In the `SaveISF` method, the first and last name values are added to the [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property of the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [Ink](/previous-versions/ms836505(v=msdn.10)) property, before the ink is serialized and written to the file.</span></span> <span data-ttu-id="786ff-128">Nachdem die frei Hand Eingaben serialisiert wurden, werden die Werte für den Vornamen und den Nachnamen aus der ExtendedProperties-Eigenschaft des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts entfernt.</span><span class="sxs-lookup"><span data-stu-id="786ff-128">After the ink has been serialized, the first and last name values are removed from the [Ink](/previous-versions/aa515768(v=msdn.10)) object's ExtendedProperties property.</span></span>


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



## <a name="saving-to-an-xml-file"></a><span data-ttu-id="786ff-129">Speichern in einer XML-Datei</span><span class="sxs-lookup"><span data-stu-id="786ff-129">Saving to an XML File</span></span>

<span data-ttu-id="786ff-130">In der- `SaveXML` Methode wird ein [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) -Objekt verwendet, um ein XML-Dokument zu erstellen und in dieses zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="786ff-130">In the `SaveXML` method, an [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) object is used to create and write to an XML document.</span></span> <span data-ttu-id="786ff-131">Mithilfe der [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts wird die frei Hand Eingabe in ein Base64-codiertes, serialisiertes frei Hand Format-Bytearray konvertiert. Anschließend wird das Bytearray in eine Zeichenfolge konvertiert, die in die XML-Datei geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="786ff-131">Using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, the ink is first converted to a base64 encoded Ink Serialized Format byte array, and then the byte array is converted to a string to be written out to the XML file.</span></span> <span data-ttu-id="786ff-132">Die Textdaten aus dem Formular werden auch in die XML-Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="786ff-132">The text data from the form is also written out to the XML file.</span></span>


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



## <a name="saving-to-an-html-file"></a><span data-ttu-id="786ff-133">Speichern in einer HTML-Datei</span><span class="sxs-lookup"><span data-stu-id="786ff-133">Saving to an HTML File</span></span>

<span data-ttu-id="786ff-134">Die SaveHtml-Methode verwendet das umgebende Feld der [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung, um zu testen, ob eine Signatur vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="786ff-134">The SaveHTML method uses the bounding box of the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection to test for the presence of a signature.</span></span> <span data-ttu-id="786ff-135">Wenn die Signatur vorhanden ist, wird Sie mithilfe der [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode des Ink-Objekts in das befestigte GIF-Format konvertiert und in eine Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="786ff-135">If the signature exists, it is converted to the fortified GIF format using the ink object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, and written to a file.</span></span> <span data-ttu-id="786ff-136">Auf das GIF wird dann in der HTML-Datei verwiesen.</span><span class="sxs-lookup"><span data-stu-id="786ff-136">The GIF is then referenced in the HTML file.</span></span>


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



## <a name="loading-a-file"></a><span data-ttu-id="786ff-137">Laden einer Datei</span><span class="sxs-lookup"><span data-stu-id="786ff-137">Loading a File</span></span>

<span data-ttu-id="786ff-138">Die- `OpenMenu_Click` Methode behandelt das Dialogfeld öffnen, öffnet die Datei und ruft die Lademethode auf, die der Auswahl des Benutzers entspricht.</span><span class="sxs-lookup"><span data-stu-id="786ff-138">The `OpenMenu_Click` method handles the Open dialog box, opens the file, and calls the loading method that corresponds to the user's choice.</span></span>

## <a name="loading-an-isf-file"></a><span data-ttu-id="786ff-139">Laden einer ISF-Datei</span><span class="sxs-lookup"><span data-stu-id="786ff-139">Loading an ISF File</span></span>

<span data-ttu-id="786ff-140">Die `LoadISF` -Methode liest die zuvor erstellte Datei und konvertiert das Bytearray mit der [Load](/previous-versions/ms569609(v=vs.100)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts in frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="786ff-140">The `LoadISF` method reads the previously created file and converts the Byte array to ink with the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="786ff-141">Der Ink Collector wird vorübergehend deaktiviert, um ihm das Ink-Objekt zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="786ff-141">The ink collector is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="786ff-142">Die `LoadISF` Methode überprüft dann die [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) -Eigenschaft des Ink-Objekts für die vor-und Nachnamen-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="786ff-142">The `LoadISF` method then checks the Ink object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property for the first and last name strings.</span></span>


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



## <a name="loading-an-xml-file"></a><span data-ttu-id="786ff-143">Laden einer XML-Datei</span><span class="sxs-lookup"><span data-stu-id="786ff-143">Loading an XML File</span></span>

<span data-ttu-id="786ff-144">Die `LoadXML` -Methode lädt eine zuvor erstellte XML-Datei, ruft Daten aus dem Ink-Knoten ab und konvertiert die Daten im Knoten mithilfe der [Load](/previous-versions/ms569609(v=vs.100)) -Methode des [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekts in Ink.</span><span class="sxs-lookup"><span data-stu-id="786ff-144">The `LoadXML` method loads a previously created XML file, retrieves data from the Ink node, and converts the data in the node to ink using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="786ff-145">Der [InkCollector](/previous-versions/ms836493(v=msdn.10)) wird vorübergehend deaktiviert, um ihm das Ink-Objekt zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="786ff-145">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="786ff-146">Das Signatur Feld wird für ungültig erklärt, und die vor-und Nachnamen-Informationen werden aus dem XML-Dokument abgerufen.</span><span class="sxs-lookup"><span data-stu-id="786ff-146">The signature box is invalidated, and the first and last name information is retrieved from the XML document.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="786ff-147">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="786ff-147">Closing the Form</span></span>

<span data-ttu-id="786ff-148">Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="786ff-148">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object.</span></span>

 

 
