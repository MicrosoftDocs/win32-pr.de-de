---
description: In diesem C- \# Beispiel wurde ein Papierformular als Portable Network Graphics (PNG-Datei) gescannt und zur Laufzeit als Hintergrundbild für ein InkPicture-Steuerelement angegeben. Im Beispiel wird ein Meldungs Feld verwendet, um Handschrift Erkennungsergebnisse anzuzeigen.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Beispiel für gescannte Papier Form
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360678"
---
# <a name="scanned-paper-form-sample"></a>Beispiel für gescannte Papier Form

In diesem C- \# Beispiel wurde ein Papierformular als Portable Network Graphics (PNG-Datei) gescannt und zur Laufzeit als Hintergrundbild für ein [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement angegeben. Im Beispiel wird ein Meldungs Feld verwendet, um Handschrift Erkennungsergebnisse anzuzeigen.

Das Beispiel enthält eine Extensible Markup Language-Datei (XML) Formdata.xml. Die XML-Datei enthält den Namen der PNG-Datei. Sie enthält auch `FieldInfo` Elemente, die rechteckige Bereiche in dem Formular definieren, in dem ein Benutzer Freihand eingeben kann. Die Informationen im- `FieldInfo` Element werden im folgenden Beispiel gezeigt:


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



Die Elemente "Left", "Top", "Right" und "Bottom" sind Definitionen von Pixelkoordinaten für jedes Feld.

Im Beispiel wird ein neues [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) mit den in Formdata.xml enthaltenen Daten initialisiert:


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



Das in Formdata.xml angegebene Formular Bild wird als Hintergrund des [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuer Elements geladen:


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



Die frei Hand Auflistung wird dann für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement aktiviert:


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a>Menü Ereignishandler

Die Anwendung umfasst Click-Ereignishandler für alle Menüs, die am oberen Rand des Formulars angezeigt werden.

### <a name="recognize-menu-item"></a>Menü Element "erkennen"

Der Menübefehl zum Erkennen von Click-Ereignis Handlern deaktiviert die frei Hand Auflistung für das Steuerelement und überprüft die Handschrifterkennung. Wenn keine Erkennung installiert ist, wird ein Dialogfeld angezeigt. Ein Benutzer muss dann auf die Menüoption "Ink" oder "Pen" klicken, um das Steuerelement für die frei Hand Eingabe erneut zu aktivieren

Wenn eine Erkennung installiert ist, ruft die `Recognize` Funktion die XML-Daten ab, die Pixelkoordinaten für jedes Formularfeld angeben. Die Koordinaten werden in Freihand Raumkoordinaten konvertiert, und für jedes Formularfeld wird ein Rechteck definiert. Nachdem Rechtecke definiert wurden, sucht die Funktion die Striche, die sich überschneiden und innerhalb jedes Rechtecks liegen. Zum Schluss führt Sie eine Erkennung der frei Hand Eingaben durch und zeigt die Ergebnisse in einem Meldungs Feld an.

### <a name="ink-menu-item"></a>Ink-Menü Element

Das Handschrift-Ereignishandler aktiviert das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement.

### <a name="pen-menu-item"></a>Stift-Menü Element

Der Ereignishandler für den Stift Menübefehl führt die folgenden Aufgaben aus:

-   Deaktiviert die frei Hand Auflistung für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement (Dies ist erforderlich, bevor die [EditingMode](/previous-versions/ms582189(v=vs.100)) -Eigenschaft geändert wird).
-   Legt die [EditingMode](/previous-versions/ms582189(v=vs.100)) -Eigenschaft zum Erfassen von frei Hand Eingaben fest.
-   Aktiviert die frei Hand Auflistung für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement erneut und schaltet die Menüs "Pen", "Select" und "Eraser" um, um den aktiven Modus anzugeben.

### <a name="edit-menu-item"></a>Menü Element bearbeiten

Der Ereignishandler für den Menübefehl Bearbeiten ähnelt dem Ereignishandler für den Stift-Menü. Sie führt die folgenden Aufgaben aus:

-   Deaktiviert die frei Hand Auflistung.
-   Legt die [EditingMode](/previous-versions/ms582189(v=vs.100)) -Eigenschaft auf **Select** fest. Dadurch kann der Benutzer die frei Handauswahl ausführen.
-   Aktiviert die frei Hand Auflistung und schaltet die Menü Stift-, Bearbeitungs-und eramingmenüs um, um den aktiven Modus anzugeben.

### <a name="eraser-menu-item"></a>Menü Element "Eraser"

Mit dem Menübefehl zum durch Klicken auf den Ereignishandler wird das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement [EditingMode](/previous-versions/ms582189(v=vs.100)) auf **Delete** festgelegt, sodass ein Benutzer frei Hand Eingaben löschen kann. Außerdem schaltet er die Menü Elemente Pen, Edit und Eraser um.

### <a name="clear-menu-item"></a>Menü Element löschen

Der Menübefehl zum Löschen des Menüs löschen löscht die aktuelle [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement und löscht dadurch alle frei Hand Eingaben im Formular.

## <a name="closing-the-form"></a>Schließen des Formulars

Im vom Windows Form-Designer generierten Code wird das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird. Wenn das Formular geschlossen wird, wird das InkPicture-Steuerelement und die anderen Komponenten des Formulars [von der verwerfen](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) -Methode des Formulars entfernt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InkEdit-Steuerelement](inkedit-control.md)
</dt> <dt>

[InkPicture-Steuerelement](inkpicture-control.md)
</dt> </dl>

 

 
