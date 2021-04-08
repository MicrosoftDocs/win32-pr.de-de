---
description: Das Beispiel "Advanced Recognition" veranschaulicht erweiterte Features der Microsoft Tablet PC Automation Application Programming Interface (API), die für die Handschrifterkennung verwendet wird.
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Beispiel für erweiterte Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e23a078ded9c6967f8e45780f8cb3a739b246f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749120"
---
# <a name="advanced-recognition-sample"></a>Beispiel für erweiterte Erkennung

Das Beispiel "Advanced Recognition" veranschaulicht erweiterte Features der Microsoft Tablet PC Automation Application Programming Interface (API), die für die Handschrifterkennung verwendet wird.

Es umfasst die folgenden Features:

-   Auflisten der installierten Erkennung
-   Erstellen eines Erkennungs Kontexts mit einer bestimmten Sprache
-   Verwenden des Erkennungs Objekts
-   Festlegen der Faktoid-und Word-Listen für Erkennung
-   Verwenden von Führungslinien zum Verbessern der Erkennungsqualität
-   Dynamische Hintergrund Erkennung
-   Gestenerkennung

Die verwendeten Schnittstellen sind: [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer), **iinkrecocontext**, [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult), **iinkrecognitionguide**, **iinkwordlist**, [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture), **iinkcollector**, **IInkDisp**, **iinkrenderer**, **iinkdrawingattributes**, **iinkstrokes** und **iinkstroke**.

## <a name="ink-and-project-headers"></a>Freihand-und Projekt Header

Fügen Sie zunächst die Header für die Schnittstellen von Tablet PC Automation ein. Diese werden mit dem Tablet PC Platform SDK installiert. Die Datei "tpcerror. h" enthält die Fehler Code Definitionen der Tablet PC-API.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



Die Eventsinks. h-Datei definiert die **iinkeventsimpl** -und die **iinkrecognitioneventsimpl** -Schnittstelle und richtet die [**erkentionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md)-, [**Stroke**](inkcollector-stroke.md)-und [**Gesten**](inkcollector-gesture.md) -Ereignisse ein.


```C++
#include "EventSinks.h"
```



Die Datei childwnds. h enthält die Definitionen der Klassen **cinkinputwnd** und **krecooutputwnd**, die von der CWindowImpl-Datei der ATL abgeleitet und zum Erstellen der untergeordneten Fenster des Beispiels verwendet werden.


```C++
#include "ChildWnds.h"
```



In der Datei "advreco. h" wird die **cadvrecoapp** -Klasse deklariert, die die Anwendungsfenster Klasse für dieses Beispiel ist.


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>Initialisieren des Anwendungsfensters

Die-Methode des Fensters `Run` richtet das **cadvrecoapp** -Objekt ein, lädt das Menü und das Symbol für das Fenster, erstellt ein [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt für die Standard Erkennung und startet die Nachrichten Schleife des Fensters.

Die **OnCreate** -Methode des Fensters behandelt das **WM \_ Create** -Ereignis und erstellt die untergeordneten Fenster. Ein [**InkCollector**](inkcollector-class.md) -Objekt stellt eine Verbindung mit der Ereignis Quelle des Ink Collector her und aktiviert frei Hand Eingaben im Eingabefenster. Anschließend wird ein [**InkRecognizerGuide**](inkrecognizerguide-class.md) -Objekt erstellt, und die [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) -Eigenschaft des frei Hand Sammlers wird verwendet, um die Rechtecke des Erkennungs Handbuchs in frei Hand Raum zu konvertieren. Schließlich erstellt die **OnCreate** -Methode ein [**inkwordlist**](inkwordlist-class.md) -Objekt.

## <a name="handling-ink-collector-events"></a>Behandeln von Ink Collector-Ereignissen

Die **OnStroke** -Methode des Fensters behandelt das [**Stroke**](inkcollector-stroke.md) -Ereignis des Ink Collector. Das neue [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt wird den [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) -Eigenschaft des Ink Collector hinzugefügt.

Die **ongesten** -Methode des Fensters behandelt das [**Gesten**](inkcollector-gesture.md) Ereignis des frei Hand Sammlers. Die **ongesten** -Methode identifiziert die Geste, verwendet die höchste Vertrauens Bewegung zuerst und überprüft, ob das Fenster diese bestimmte Geste unterstützt. Wenn die Geste unterstützt wird, wird das umgebende Feld der Geste für ungültig erklärt, da die Geste aus der Striche-Auflistung entfernt wird. Wenn die Geste nicht unterstützt wird, wird das **Gesten** Ereignis abgebrochen, was bewirkt, dass der Ink Collector ein [**Stroke**](inkcollector-stroke.md) -Ereignis auslöst. Schließlich wird das Fenster mit den Ergebnissen aktualisiert.

## <a name="handling-recognizer-context-events"></a>Behandeln von Erkennungs Kontext Ereignissen

Die **onerkentionwithalternative es** -Methode des Fensters behandelt das Ereignis " [**erkenntionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md) " des Erkennungs Moduls. Die **onerkentionwithalternativen** -Methode zeigt die Erkennungsergebnisse im Fenster "Ergebnisse" an.

## <a name="handling-menu-commands"></a>Behandeln von Menübefehlen

Die **onerkenzer** -Methode des Fensters verarbeitet die Befehle im Erkennungs Menü. Wenn der **Standard** Befehl ausgewählt wurde, wird die [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) -Methode von [inkrecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) zum Abrufen der Standard Erkennung verwendet. Andernfalls wird die ausgewählte Erkennung abgerufen. Anschließend wird ein Erkennungs Kontext erstellt und verwendet, und Menü-und Statusleiste werden aktualisiert.

Die **onfactoidwordlist** -Methode des Fensters verarbeitet den **use WordList** -Befehl im **Factoid** -Menü. Die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft der Erkennungs Kontext wird auf **null** festgelegt, um den Erkennungs Kontext zurückzusetzen. Wenn die Option **use WordList** deaktiviert ist, wird die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -Eigenschaft der Erkennungsfunktion auf **null** festgelegt. Andernfalls wird die **WordList** -Eigenschaft des Erkennungs Kontexts auf die [**inkwordlist**](inkwordlist-class.md) festgelegt, die in der **OnCreate** -Methode erstellt wurde. Schließlich werden die [inkstriche](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des Ink Collector erneut an den Erkennungs Kontext angefügt, die [**backgrounderkennzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) -Methode der Erkennungsfunktion wird aufgerufen, und das Menü wird aktualisiert.

Die **onfactoid** -Methode des Fensters behandelt die Factoid-Befehle im **Factoid** -Menü. Zuerst wird die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft des erkentekontexts auf **null** festgelegt, die " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) "-Eigenschaft des erkentekontexts wird auf die ausgewählte "Faktoid" festgelegt, und die [inkstriche](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des frei Hand Sammlers werden dem Erkennungs Kontext neu zugewiesen. Wenn das [Factoid](factoid-constants.md) -Objekt vom Erkennungs Kontext unterstützt wird, wird die [**backgrounderkennzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) -Methode der Erkennungsfunktion aufgerufen. Andernfalls wird eine Fehlermeldung angezeigt. Zum Schluss werden das Menü und die Statusleiste aktualisiert.

Die **OnGuide** -Methode des Fensters behandelt die Befehle im Menü " **Guide** ". Wenn der erkenerungkontext die-Führungs Optionen unterstützt, legt die **OnGuide** -Methode die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft der Erkennungsfunktion auf **null** fest, legt die " [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) "-Eigenschaft des Erkennungs-Kontexts auf die ausgewählte Führungs Einstellung fest, weist die [inkstriche](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) des frei Hand Sammlers dem Erkennungs Programmkontext zu und ruft die [**backgrounderkenzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) -Methode des Erkennungs Kontexts auf. Andernfalls wird eine Fehlermeldung angezeigt. Zum Schluss werden das Eingabefenster, das Menü und die Statusleiste aktualisiert.

Die **onmode** -Methode des Fensters verarbeitet die Befehle im Menü **Modus** . Sie deaktiviert den Ink Collector, aktualisiert die [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) -Eigenschaft des Ink Collector, aktualisiert das Menü und zeigt die Gesten Listen an oder blendet sie aus. Schließlich ist der frei Hand Sammler aktiviert.

Die **onerkenenmethode** des Fensters verarbeitet den Befehl " **erkennen** " im frei Hand Menü. Sie ruft die [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) -Methode der Erkennungs Kontext Methode auf, um das Hinzufügen von frei Hand Eingaben zum Erkennungs Kontext beizubehalten. Dies ist manchmal erforderlich, da nicht alle Erkennungs Tools partielle Erkennung unterstützen. Anschließend wird die [**Erkennungsmethode des**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) Erkennungs Kontexts aufgerufen, und die Ergebnisse werden an die **onerkentionwithalternativen** -Methode des Fensters weitergeleitet. Schließlich wird der [InkCollector](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) der Ink Collector dem Erkennungs Kontext zugewiesen.

Die **OnClear** -Methode des Fensters **verarbeitet den Befehl** Clear im **frei Hand** Menü. Die Striche werden aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) -Eigenschaft des frei Hand Sammlers gelöscht, die alte Striche-Auflistung und eine neue für die **Ink-Eigenschaft** des frei Hand Sammlers erstellt und die neue Strokes-Auflistung an den Erkennungs Kontext angefügt.

Die **OnExit** -Methode des Fensters verarbeitet den **Exit** -Befehl **im frei Hand Menü und** löst das \_ Ereignis "Close" aus.

## <a name="helper-methods"></a>Hilfsmethoden

Die **loadmenu** -Methode des Fensters wird von der **Run** -Methode des Fensters aufgerufen und fügt die Liste der unterstützten erkenungen und die Liste der unterstützten factoide zum Menü hinzu. Zuerst werden die [inkrecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85))abgerufen. Anschließend werden die verfügbaren erkenzer durchlaufen, und nur diejenigen, die eine Liste von Sprachen in der Eigenschaft **Languages** enthalten, werden dem **Erkennungs** Menü hinzugefügt. Schließlich wird das Menü " **Faktoid** " mit der Liste der als globale Konstante definierten Faktoide aufgefüllt.

Die **userecognizer** -Methode des Fensters wird von der **onerkenzer** -Methode des Fensters aufgerufen, wenn der Benutzer eine neue Erkennung auswählt. Dabei wird ein Erkennungs Kontext erstellt, der alte Kontext von der Erkennungs Ereignis Senke getrennt, der alte Kontext gelöscht und freigegeben, und der neue Kontext wird an die Erkennungs Ereignis Senke angefügt.

Anschließend prüft die **userecognizer** -Methode die [**Funktionen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) -Eigenschaft der Erkennung, die einen [**inkrecognizerfunction-**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) Wert zurückgibt. Wenn die Erkennung eine Inline Eingabe unterstützt, ist der Befehl **Zeilen** im Menü " **Guide** " aktiviert. Wenn die Erkennung eine eingegebene Eingabe unterstützt, ist der **Boxes** -Befehl aktiviert. Wenn die Erkennung keine kostenlose Eingabe unterstützt, ist der Befehl **None** deaktiviert. Wenn die Auswahl des aktuellen Handbuchs nicht unterstützt wird, werden sowohl die Eigenschaft [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) des Erkennungs Kontexts als auch das Menü aktualisiert.

Anschließend versucht die **userecognizer** -Methode, die [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) -und [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) -Eigenschaften des Erkennungs Kontexts festzulegen. Wenn eine der beiden Einstellungen von der Erkennung nicht unterstützt wird, wird der Standardwert verwendet, und das Menü wird aktualisiert.

Schließlich fügt die **userecognizer** -Methode die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft des [**InkDisp**](inkdisp-class.md) -Objekts des Ink Collector an den Erkennungs Kontext an, ändert die Schriftart des Ausgabe Fensters in eine, die von der Sprache der Erkennung unterstützt wird, setzt das Ausgabefenster zurück und aktualisiert die Erkennungsergebnisse durch Aufrufen der [**backgrounderkennerkenzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) -Methode des Erkennungs Kontexts.

Die **getgesturename** -Methode des Fensters wird von der **ongesten** -Methode des Fensters aufgerufen. Er sucht nach der Geste und gibt einen Index an den Namen der Geste zurück, der in einer Zeichen folgen Tabelle in der Datei "advreco. RC" gespeichert ist.

 

 
