---
description: Dieses Beispiel baut auf dem Beispiel "Auto Claims Form" auf, indem das PenInputPanel-Objekt integriert wird. Das Beispiel befindet sich im Verzeichnis C \# PIPanel im Ordner AutoClaims.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: PenInputPanel-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c464be52fd08c6c461ba094428a1868fbb51fb328e1a3c88a2d0949a6ae581e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934740"
---
# <a name="peninputpanel-sample"></a>PenInputPanel-Beispiel

Dieses Beispiel baut auf dem Beispiel "Auto Claims Form" auf, indem das [PenInputPanel-Objekt integriert](/previous-versions/aa514041(v=msdn.10)) wird. Das Beispiel befindet sich im Verzeichnis C \# PIPanel im Ordner AutoClaims.

> [!Note]  
> Dieses Beispiel erfordert, dass Ihr System mit einem Stiftgerät ausgestattet ist. Wenn Sie nur eine Maus (oder ein anderes nicht menschliches Schnittstellengerät (HID) verwenden, das auf das Gerät zeigen soll, wird [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) nicht angezeigt.

 

Weitere Informationen zum Beispiel für das Formular für automatische Ansprüche finden Sie unter [Auto Claims Form Sample](auto-claims-form-sample.md). Weitere Informationen zum [PenInputPanel-Objekt finden](/previous-versions/aa514041(v=msdn.10)) Sie unter [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).

Im Beispiel enthält das Formular für automatische Ansprüche fünf Felder, in denen der Benutzer aufgefordert wird, informationen zu geben, die für den Anspruch relevant sind: Richtliniennummer, Name des Vornamens, Jahr, Make und Modell des Autos. Ein [PenInputPanel-Objekt](/previous-versions/aa514041(v=msdn.10)) wird an jedes Eingabefeld angefügt, um eine einfache Möglichkeit zum Eingeben von Werten mit einem Stift zu bieten.

Es gibt zwei Verfahren zum Anfügen eines [PenInputPanel-Objekts](/previous-versions/aa514041(v=msdn.10)) an die Eingabefelder im Formular. Die erste Technik besteht in der Zuweisung einer separaten Instanz des -Objekts zu jedem Eingabefeld zur Entwurfszeit. Die zweite besteht in der Erstellung einer einzelnen Instanz des -Objekts und dem anschließenden Anfügen dieser Objektinstanz zur Laufzeit an ein Feld, wenn es den Fokus erhält. In diesem Beispiel werden beide Techniken veranschaulicht.

Bei der Entscheidung, welche Technik verwendet werden soll, gibt es Vor- und Abkniff. Das Erstellen einer eindeutigen Instanz des -Objekts für jedes Formularfeld erfordert etwas mehr Arbeitsspeicher, wenn das Formular geladen wird. Es erspart sich jedoch die Handhabung von Fokusereignissen für die Felder, um dem aktuellen Feld zur Laufzeit eine einzelne Instanz zu zuweisen.

Da das [PenInputPanel-Objekt](/previous-versions/aa514041(v=msdn.10)) nur auf einem Tablet-PC unterstützt wird, erstellt das Beispiel die PenInputPanel-Objekte innerhalb eines Ausnahmebehandlungsblocks.

## <a name="one-object-per-field"></a>Ein Objekt pro Feld

Das Beispiel veranschaulicht die erste Technik (ein [PenInputPanel-Objekt](/previous-versions/aa514041(v=msdn.10)) pro Feld), indem die Eingabefelder für die Richtliniennummer ( ) und den Namen des Vornamens ( ) einer eindeutigen Instanz des `inkEdPolicyNumber` `inkEdName` PenInputPanel-Objekts zugewiesen werden. Ein überladener Konstruktor für das PenInputPanel-Objekt kann den Namen des Eingabesteuerelementes als Argument verwenden und so die Steuerelemente zuordnen. Die folgenden Zeilen aus [](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) dem Load-Ereignishandler des Formulars zeigen Folgendes:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Ein Objekt pro Formular

Das zweite Verfahren wird auch im Beispiel gezeigt: Eine einzelne Instanz eines [PenInputPanel-Objekts,](/previous-versions/aa514041(v=msdn.10)) , wird von den Eingabefeldern Year, Make und `pipShared` Model gemeinsam genutzt. Das freigegebene Objekt wird mithilfe des Standardkonstruktors erstellt.


```C++
pipShared = new PenInputPanel();
```



Die Verwendung dieser Technik erfordert, dass ihr Formular nur über eine einzelne Instanz des [PenInputPanel-Objekts](/previous-versions/aa514041(v=msdn.10)) verfügen muss. Dies spart Arbeitsspeicher, aber Sie müssen Code hinzufügen, um das Ereignis zu behandeln, wenn ein Eingabefeld den Fokus erhält. Wenn ein Steuerelement, das eine freigegebene Instanz eines PenInputPanel-Objekts verwendet, den Fokus erhält, legen Sie die [AttachedEditControl-Eigenschaft](/previous-versions/aa514050(v=msdn.10)) des PenInputPanel-Objekts auf dieses Steuerelement fest. Der folgende Code zeigt einen Ereignishandler für die Ereignisse der Felder Year, Make und `Enter` Model.


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



Achten Sie darauf, dass Sie alle Eigenschaften festlegen, die festgelegt werden müssen, wenn sich der Fokus auf ein neues Steuerelement ändert. In den vorherigen Ereignishandlern wird beispielsweise die [Factoid-Eigenschaft](/previous-versions/ms571978(v=vs.100)) entsprechend festgelegt.

## <a name="usability-considerations"></a>Überlegungen zur Benutzerfreundlichkeit

Beachten Sie bei der Verwendung des [PenInputPanel-Objekts](/previous-versions/aa514041(v=msdn.10)) in Ihrer Anwendung die folgenden Überlegungen zur Benutzerfreundlichkeit.

### <a name="positioning-the-peninputpanel"></a>Positionieren des PenInputPanel

Da die Felder in diesem Beispiel vertikal auf dem Formular angeordnet sind, wird die [PenInputPanel-Benutzeroberfläche](/previous-versions/aa514041(v=msdn.10)) für jedes Eingabesteuerfeld leicht rechts neben dem Eingabesteuerfeld positioniert, um die Verwendung zu vereinfachen. Dadurch wird verhindert, dass penInputPanel das nächste Bearbeitungsfeld überdeckt, wodurch es einfacher wird, das nächste Bearbeitungsfeld als Ziel zu verwenden.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Auswählen des anzuzeigenden Eingabebereichs

Da Richtliniennummern häufig Kombinationen aus Zahlen, Buchstaben und anderen Zeichen sind, können sie anfällig für Erkennungsfehler sein. Daher legt das Beispiel den Standardbereich, der vom [PenInputPanel-Objekt](/previous-versions/aa514041(v=msdn.10)) angezeigt wird, auf die Tastatur fest, wenn er an das Feld mit der Richtliniennummer angefügt wird.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



Das Standardverhalten des [PenInputPanel-Objekts](/previous-versions/aa514041(v=msdn.10)) ist die Verwendung des Panels, den der Benutzer zuletzt ausgewählt hat.

### <a name="text-services-framework-correction-user-interface"></a>Textdienstframework Korrektur Benutzeroberfläche

In diesem Beispiel sind alle Eingabefelder [InkEdit-Steuerelemente.](/previous-versions/ms552265(v=vs.100)) Dies ist wichtig, da das InkEdit-Steuerelement über integrierte Unterstützung für die [Textdienstframework](../tsf/text-services-framework.md) (TSF) verfügt und daher die benutzeroberfläche für die Korrektur für Eingaben unterstützen kann, die vom [PenInputPanel-Objekt empfangen](/previous-versions/aa514041(v=msdn.10)) werden.

Der Standardwert für [EnableTsf](/previous-versions/ms569656(v=vs.100)) ist **TRUE.** Dies bewirkt, dass das [PenInputPanel-Objekt](/previous-versions/aa514041(v=msdn.10)) versucht, die Textdienstframework (TSF) auf dem angefügten Steuerelement zu starten. Bei Erfolg wird die Korrektur-Benutzeroberfläche im -Steuerelement angezeigt und ermöglicht den Zugriff auf Erkennungswechsel. Wenn Sie diese Methode mit einem **FALSE-Parameter** aufrufen, wird versucht, tsf für das angefügte Steuerelement herunterzufahren.

Das [InkEdit-Steuerelement](/previous-versions/ms552265(v=vs.100)) bietet bereits eine Korrektur-Benutzeroberfläche, aber im Beispiel wird [EnableTsf](/previous-versions/ms569656(v=vs.100)) verwendet, um [dem PenInputPanel](/previous-versions/aa514041(v=msdn.10)) die Verwendung des TSF-Einfügeerkennungskontexts anstelle der [**SendInput-Funktion**](/windows/win32/api/winuser/nf-winuser-sendinput) zu ermöglichen, um die Handschrifterkennungsergebnisse an das Steuerelement zu senden. Das Ergebnis ist, dass Text auch dann eingefügt werden kann, wenn das Feld nicht mehr den Fokus besitzt.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Schließen des Formulars

Im Windows des Formular-Designers werden die Steuerelemente [InkEdit](/previous-versions/ms552265(v=vs.100)) und [InkPicture](/previous-versions/aa514604(v=msdn.10)) der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird. Wenn das Formular geschlossen wird, werden die Steuerelemente InkEdit und InkPicture sowie die anderen Komponenten des Formulars durch die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) des Formulars verworfen. Die Dispose-Methode des Formulars [](/previous-versions/aa515768(v=msdn.10)) gibt auch die Fürk-Objekte zurück, die für das Formular erstellt werden.

 

 
