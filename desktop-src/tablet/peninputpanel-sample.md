---
description: Dieses Beispiel baut auf dem Formular Beispiel für automatische Ansprüche auf, indem das Objekt "pinputpanel" integriert wird. Das Beispiel befindet sich im Verzeichnis "C \# pipanel" im Ordner "autoclaims".
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Beispiel für "pinputpanel"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369825"
---
# <a name="peninputpanel-sample"></a>Beispiel für "pinputpanel"

Dieses Beispiel baut auf dem Formular Beispiel für automatische Ansprüche auf, indem das Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " integriert wird. Das Beispiel befindet sich im Verzeichnis "C \# pipanel" im Ordner "autoclaims".

> [!Note]  
> Für dieses Beispiel ist es erforderlich, dass das System mit einem Stift Gerät ausgestattet ist. Wenn Sie nur eine Maus verwenden (oder ein anderes Gerät, das kein Personal Interface (HID) ist), wird das " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " nicht angezeigt.

 

Weitere Informationen zum Beispiel für ein automatisches Anspruchsformular finden Sie unter [Beispiel für automatisches Anspruchsformular](auto-claims-form-sample.md). Weitere Informationen zum Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " finden [Sie unter Programmieren des Eingabe Panels mithilfe der Klasse "pinputpanel](programming-the-input-panel-using-the-peninputpanel-class.md)".

Im Beispiel enthält das Formular für automatische Ansprüche fünf Felder, in die der Benutzer aufgefordert wird, relevante Informationen für den Anspruch zu platzieren: Richtlinien Nummer, Name des Versicherten, Jahr, Marke und Modell des Autos. Ein [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) -Objekt wird an jedes Eingabefeld angehängt, um eine einfache Möglichkeit zum Eingeben von Werten mit einem Stift zu bieten.

Es gibt zwei Verfahren zum Anfügen eines " [larinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts an die Eingabefelder in Ihrem Formular. Die erste Methode besteht darin, jedem Eingabefeld zur Entwurfszeit eine separate Instanz des-Objekts zuzuweisen. Die zweite besteht darin, eine einzelne Instanz des Objekts zu erstellen und diese Objektinstanz zur Laufzeit an ein Feld anzufügen, wenn Sie den Fokus erhält. In diesem Beispiel werden beide Methoden veranschaulicht.

Es gibt Kompromisse bei der Entscheidung, welches Verfahren Sie verwenden sollten. Das Erstellen einer eindeutigen Instanz des-Objekts für jedes Formularfeld erfordert etwas mehr Arbeitsspeicher, wenn das Formular geladen wird. Es speichert jedoch das Verarbeiten von Fokus Ereignissen für die Felder, um dem aktuellen Feld zur Laufzeit eine einzelne Instanz zuzuweisen.

Da das " [cuinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt nur auf einem Tablet PC unterstützt wird, erstellt das Beispiel die "cuinputpanel"-Objekte innerhalb eines Ausnahme Behandlungs Blocks.

## <a name="one-object-per-field"></a>Ein Objekt pro Feld

Das Beispiel veranschaulicht das erste Verfahren (ein " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt pro Feld), indem die Eingabefelder für die Richtlinien Nummer ( `inkEdPolicyNumber` ) und der Versicherte Name ( `inkEdName` ) eine eindeutige Instanz des "pinputpanel"-Objekts zugewiesen werden. Ein überladener Konstruktor für das Objekt "pinputpanel" kann den Namen des Eingabe Steuer Elements als Argument annehmen und somit die Steuerelemente zuordnen. Die folgenden Zeilen aus dem [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignishandler des Formulars zeigen Folgendes:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Ein Objekt pro Formular

Das zweite Verfahren ist auch im Beispiel dargestellt: eine einzelne Instanz eines " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts, `pipShared` , wird zwischen den Eingabefeldern "Year", "Make" und "Model" gemeinsam genutzt. Das freigegebene Objekt wird mit dem Standardkonstruktor erstellt.


```C++
pipShared = new PenInputPanel();
```



Wenn Sie dieses Verfahren verwenden, muss das Formular nur über eine einzelne Instanz [des Objekts "](/previous-versions/aa514041(v=msdn.10)) " "" "" " Dadurch wird Arbeitsspeicher gespart, aber Sie müssen Code hinzufügen, um das Ereignis zu behandeln, wenn ein Eingabefeld den Fokus erhält. Wenn ein Steuerelement, das eine freigegebene Instanz eines "pinputpanel"-Objekts verwendet, den Fokus erhält, legen Sie die Eigenschaft " [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) " des Objekts "pinputpanel" auf diese Steuer Der folgende Code zeigt einen Ereignishandler für die Ereignisse "Year", "Make" und "Model" `Enter` .


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



Stellen Sie sicher, dass Sie alle Eigenschaften festlegen, die festgelegt werden müssen, wenn Änderungen auf ein neues Steuerelement fokussiert werden. In den vorherigen Ereignis Handlern wird z. b. die Eigenschaft " [Faktoid](/previous-versions/ms571978(v=vs.100)) " entsprechend festgelegt.

## <a name="usability-considerations"></a>Nutzbarkeits Überlegungen

Berücksichtigen Sie die folgenden Überlegungen zur Benutzerfreundlichkeit, wenn Sie das Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " in Ihrer Anwendung verwenden.

### <a name="positioning-the-peninputpanel"></a>Positionieren von "pinputpanel"

Da die Felder auf dem Formular in diesem Beispiel vertikal angeordnet werden, wird die Benutzeroberfläche des Benutzer Steuer Elements für jedes Eingabe Steuerelement leicht auf der rechten Seite des Eingabe Steuer Elements positioniert, [um die Verwendung](/previous-versions/aa514041(v=msdn.10)) zu vereinfachen. Dadurch wird verhindert, dass das angriffpanel-Element das nächste Bearbeitungsfeld abdeckt, sodass das nächste Bearbeitungsfeld einfacher als Ziel ist.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Auswählen des anzuzeigenden Eingabe Panels

Da Richtlinien Nummern häufig Kombinationen aus Zahlen, Buchstaben und anderen Zeichen darstellen, können Sie zu Erkennungs Fehlern neigen. Aus diesem Grund legt das Beispiel den Standardbereich fest, [der vom Objekt "](/previous-versions/aa514041(v=msdn.10)) -ID" als Tastatur angezeigt wird, wenn es an das Feld "Richtlinien Nummer" angefügt wird.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



Das Standardverhalten des " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts besteht darin, den Bereich zu verwenden, der vom Benutzer zuletzt ausgewählt wurde.

### <a name="text-services-framework-correction-user-interface"></a>Benutzeroberfläche für die Korrektur von Text Services Framework

In diesem Beispiel sind alle Eingabefelder [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelemente. Dies ist wichtig, da das InkEdit-Steuerelement über eine integrierte Unterstützung für das [Text Services-Framework](../tsf/text-services-framework.md) (TSF) verfügt und daher in der Lage ist, die Benutzeroberfläche für die direkte Korrektur für Eingaben zu unterstützen, die vom Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " empfangen werden.

Der Standardwert für [enabletsf](/previous-versions/ms569656(v=vs.100)) ist " **true**". Dies bewirkt, dass das Objekt " [tzinputpanel](/previous-versions/aa514041(v=msdn.10)) " versucht, das Text Dienst Framework (TSF) im angefügten Steuerelement zu starten. Bei erfolgreicher Ausführung zeigt die Benutzeroberfläche für Korrekturen im-Steuerelement an und ermöglicht den Zugriff auf Erkennungs Alternativen. Wenn Sie diese Methode mit einem **false** -Parameter aufrufen, wird TSF für das angefügte Steuerelement heruntergefahren.

Das [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelement stellt bereits eine Korrektur Benutzeroberfläche bereit, aber im Beispiel wird [enabletsf](/previous-versions/ms569656(v=vs.100)) verwendet, [um die Verwendung](/previous-versions/aa514041(v=msdn.10)) des TSF-einfügeerkennungskontexts anstelle der [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) -Funktion zu ermöglichen, um die Handschrift Erkennungsergebnisse an das Steuerelement zu senden. Das Ergebnis ist, dass Text eingefügt werden kann, auch wenn das Feld nicht mehr den Fokus besitzt.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Schließen des Formulars

Im vom Windows Form-Designer generierten Code werden die Steuerelemente [InkEdit](/previous-versions/ms552265(v=vs.100)) und [InkPicture](/previous-versions/aa514604(v=msdn.10)) der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird. Wenn das Formular geschlossen wird, werden die InkEdit-und InkPicture-Steuerelemente sowie die anderen Komponenten des Formulars von der [verwerfen-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) des Formulars entfernt. Die verwerfen-Methode des Formulars gibt auch die frei [Hand Objekte frei, die für](/previous-versions/aa515768(v=msdn.10)) das Formular erstellt werden.

 

 
