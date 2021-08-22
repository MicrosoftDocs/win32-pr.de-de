---
title: Vorgänge in der Zwischenablage
description: Ein Fenster sollte beim Ausschneiden, Kopieren oder Einfügen von Daten die Zwischenablage verwenden. Ein Fenster platziert Daten für Ausschneide- und Kopiervorgänge in der Zwischenablage und ruft Daten für Einfügevorgänge aus der Zwischenablage ab.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Windows Benutzeroberfläche, Zwischenablage
- Zwischenablage, Fenster
- Zwischenablage, Datenschneiden
- Zwischenablage,Kopieren von Daten
- Zwischenablage,Einfügen von Daten
- Zwischenablage, Besitzerfenster
- Zwischenablage, verzögertes Rendering
- Zwischenablage, Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a0dfe82f6130f0435521ac4e17cf8e8b7162115074f7b3ff716187730f8bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545434"
---
# <a name="clipboard-operations"></a>Vorgänge in der Zwischenablage

Ein Fenster sollte beim Ausschneiden, Kopieren oder Einfügen von Daten die Zwischenablage verwenden. Ein Fenster platziert Daten für Ausschneide- und Kopiervorgänge in der Zwischenablage und ruft Daten für Einfügevorgänge aus der Zwischenablage ab. In den folgenden Abschnitten werden diese Vorgänge und verwandte Probleme beschrieben.

Um Daten in der Zwischenablage zu platzieren oder Daten aus der Zwischenablage abzurufen, muss ein Fenster zuerst die Zwischenablage mithilfe der [**OpenClipboard-Funktion**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) öffnen. Nur in einem Fenster kann die Zwischenablage gleichzeitig geöffnet sein. Um herauszufinden, in welchem Fenster die Zwischenablage geöffnet ist, rufen Sie die [**GetOpenClipboardWindow-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) auf. Wenn dies abgeschlossen ist, muss das Fenster die Zwischenablage schließen, indem die [**CloseClipboard-Funktion**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) aufgerufen wird.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Ausschneide- und Kopiervorgänge](#cut-and-copy-operations)
-   [Einfügevorgänge](#paste-operations)
-   [Besitz der Zwischenablage](#clipboard-ownership)
-   [Verzögertes Rendering](#delayed-rendering)
-   [Arbeitsspeicher und Zwischenablage](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Ausschneide- und Kopiervorgänge

Um Informationen in der Zwischenablage zu platzieren, löscht ein Fenster zunächst alle vorherigen Inhalte der Zwischenablage mithilfe der [**EmptyClipboard-Funktion.**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) Diese Funktion sendet die [**WM \_ DESTROYCLIPBOARD-Nachricht**](wm-destroyclipboard.md) an den vorherigen Besitzer der Zwischenablage, gibt Ressourcen frei, die Daten in der Zwischenablage zugeordnet sind, und weist dem Fenster, in dem die Zwischenablage geöffnet ist, den Besitz der Zwischenablage zu. Um herauszufinden, welches Fenster die Zwischenablage besitzt, rufen Sie die [**GetClipboardOwner-Funktion**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) auf.

Nach dem Leeren der Zwischenablage platziert das Fenster Daten in der Zwischenablage in so vielen Zwischenablageformaten wie möglich, sortiert vom beschreibendsten Zwischenablageformat bis zum am wenigsten beschreibenden Format. Für jedes Format ruft das Fenster die [**SetClipboardData-Funktion**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) auf und gibt den Formatbezeichner und ein globales Speicherhandle an. Das Speicherhandle kann NULL sein, was angibt, dass das Fenster die Daten auf Anforderung rendert. Weitere Informationen finden Sie unter [Verzögertes Rendering.](#delayed-rendering)

## <a name="paste-operations"></a>Einfügevorgänge

Zum Abrufen von Einfügeinformationen aus der Zwischenablage bestimmt zunächst ein Fenster das abzurufende Zwischenablageformat. In der Regel listet ein Fenster die verfügbaren Zwischenablageformate mithilfe der [**EnumClipboardFormats-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) auf und verwendet das erste Format, das es erkennt. Diese Methode wählt das am besten verfügbare Format entsprechend der Priorität aus, die beim Platzieren der Daten in der Zwischenablage festgelegt wurde.

Alternativ kann ein Fenster die [**GetPriorityClipboardFormat-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) verwenden. Diese Funktion identifiziert das beste verfügbare Zwischenablageformat gemäß einer angegebenen Priorität. Ein Fenster, das nur ein Zwischenablageformat erkennt, kann mithilfe der [**IsClipboardFormatAvailable-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable) einfach bestimmen, ob dieses Format verfügbar ist.

Nach dem Bestimmen des zu verwendenden Zwischenablageformats ruft ein Fenster die [**GetClipboardData-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) auf. Diese Funktion gibt das Handle an ein globales Speicherobjekt zurück, das Daten im angegebenen Format enthält. Ein Fenster kann das Speicherobjekt kurz sperren, um die Daten zu untersuchen oder zu kopieren. Ein Fenster sollte das Objekt jedoch nicht freigeben oder für einen längeren Zeitraum gesperrt lassen.

## <a name="clipboard-ownership"></a>Besitz der Zwischenablage

Der Besitzer der *Zwischenablage* ist das Fenster, das den Informationen in der Zwischenablage zugeordnet ist. Ein Fenster wird zum Besitzer der Zwischenablage, wenn es Daten in der Zwischenablage platziert, insbesondere wenn die [**EmptyClipboard-Funktion**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) aufruft. Das Fenster bleibt der Besitzer der Zwischenablage, bis es geschlossen wird oder ein anderes Fenster die Zwischenablage leert.

Wenn die Zwischenablage geleert wird, empfängt der Besitzer der Zwischenablage eine [**WM \_ DESTROYCLIPBOARD-Meldung.**](wm-destroyclipboard.md) Im Folgenden sind einige Gründe aufgeführt, warum diese Meldung in einem Fenster verarbeitet werden kann:

-   Das verzögerte Rendern eines oder mehrerer Zwischenablageformate im Fenster. Als Reaktion auf die [**WM \_ DESTROYCLIPBOARD-Meldung**](wm-destroyclipboard.md) gibt das Fenster möglicherweise Ressourcen frei, die ihm zugewiesen wurden, um Daten auf Anforderung zu rendern. Weitere Informationen zum Rendern von Daten finden Sie unter [Verzögertes Rendering.](#delayed-rendering)
-   Das Fenster platzierte Daten in der Zwischenablage in einem privaten Zwischenablageformat. Die Daten für private Zwischenablageformate werden vom System nicht freigegeben, wenn die Zwischenablage geleert wird. Daher sollte der Besitzer der Zwischenablage die Daten nach dem Empfang der [**WM \_ DESTROYCLIPBOARD-Nachricht**](wm-destroyclipboard.md) freigeben. Weitere Informationen zu privaten Zwischenablageformaten finden Sie unter [Zwischenablageformate.](clipboard-formats.md)
-   Das Fenster platzierte Daten in der Zwischenablage mithilfe des **CF OWNERDISPLAY-Zwischenablageformats. \_** Als Reaktion auf die [**WM \_ DESTROYCLIPBOARD-Meldung**](wm-destroyclipboard.md) gibt das Fenster möglicherweise Ressourcen frei, die es zum Anzeigen von Informationen im Zwischenablage-Viewer-Fenster verwendet hat. Weitere Informationen zu diesem alternativen Format finden Sie unter [Besitzeranzeigeformat.](about-the-clipboard.md)

## <a name="delayed-rendering"></a>Verzögertes Rendering

Beim Platzieren eines Zwischenablageformats in der Zwischenablage kann ein Fenster das Rendern der Daten in diesem Format verzögern, bis die Daten benötigt werden. Zu diesem Zweck kann eine Anwendung **NULL** für den *hData-Parameter* der [**SetClipboardData-Funktion**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) angeben. Dies ist nützlich, wenn die Anwendung mehrere Zwischenablageformate unterstützt, von denen einige oder alle zeitaufwendig zum Rendern sind. Durch Übergeben eines **NULL-Handles** rendert ein Fenster komplexe Zwischenablageformate nur dann, wenn sie benötigt werden.

Wenn ein Fenster das Rendern eines Zwischenablageformats verzögert, muss es darauf vorbereitet sein, das Format auf Anforderung zu rendern, solange es der Besitzer der Zwischenablage ist. Das System sendet dem Besitzer der Zwischenablage eine [**\_ WM-RENDERFORMAT-Nachricht,**](wm-renderformat.md) wenn eine Anforderung für ein bestimmtes Format empfangen wird, das nicht gerendert wurde. Beim Empfang dieser Meldung sollte das Fenster die [**SetClipboardData-Funktion**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) aufrufen, um ein globales Speicherhandle in der Zwischenablage im angeforderten Format zu platzieren.

Eine Anwendung darf die Zwischenablage nicht öffnen, bevor [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) als Reaktion auf die [**WM \_ RENDERFORMAT-Nachricht**](wm-renderformat.md) aufgerufen wird. Das Öffnen der Zwischenablage ist nicht erforderlich, und jeder Versuch, dies zu tun, schlägt fehl, da die Zwischenablage derzeit von der Anwendung geöffnet gehalten wird, die angefordert hat, dass das Format gerendert werden soll.

Wenn der Besitzer der Zwischenablage kurz vor der Zerstörung steht und das Rendern einiger oder aller Zwischenablageformate verzögert hat, empfängt er die [**WM \_ RENDERALLFORMATS-Meldung.**](wm-renderallformats.md) Nachdem diese Meldung empfangen wurde, sollte das Fenster die Zwischenablage öffnen, mit der [**GetClipboardOwner-Funktion**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) überprüfen, ob sie weiterhin der Besitzer der Zwischenablage ist, und dann gültige Speicherhandles für alle zwischenablageformaten, die es bereitstellt, in der Zwischenablage platzieren. Dadurch wird sichergestellt, dass diese Formate verfügbar bleiben, nachdem der Besitzer der Zwischenablage zerstört wurde.

Im Gegensatz zu [**WM \_ RENDERFORMAT**](wm-renderformat.md)sollte eine Anwendung, die auf [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) reagiert, die Zwischenablage öffnen, bevor [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) aufgerufen wird, um globale Speicherhandles in der Zwischenablage zu platzieren.

Alle Zwischenablageformate, die nicht als Antwort auf die [**WM \_ RENDERALLFORMATS-Nachricht**](wm-renderallformats.md) gerendert werden, sind nicht mehr für andere Anwendungen verfügbar und werden nicht mehr von den Zwischenablagefunktionen aufgeführt.

## <a name="memory-and-the-clipboard"></a>Arbeitsspeicher und Zwischenablage

Ein Speicherobjekt, das in der Zwischenablage platziert werden soll, sollte mithilfe der [**GlobalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) mit dem **GMEM \_ MOVEABLE-Flag** zugeordnet werden.

Nachdem ein Speicherobjekt in der Zwischenablage platziert wurde, wird der Besitz dieses Speicherhandle an das System übertragen. Wenn die Zwischenablage geleert wird und das Speicherobjekt über eines der folgenden Zwischenablageformate verfügt, gibt das System das Speicherobjekt frei, indem die angegebene Funktion aufgerufen wird:



| Funktion zum Freigeben von Objekten                             | Format der Zwischenablage                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ DSPENHMETAFILE**<br/> **CF \_ DSPMETAFILEPICT**<br/> **CF \_ ENHMETAFILE**<br/> **CF \_ METAFILEPICT**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **CF \_ BITMAP**<br/> **CF \_ DSPBITMAP**<br/> **CF \_ PALETTE**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **CF \_ DIB**<br/> **CF \_ DIBV5**<br/> **CF \_ DSPTEXT**<br/> **CF \_ OEMTEXT**<br/> **CF \_ TEXT**<br/> **CF \_ UNICODETEXT**<br/>   |
| Keine<br/>                                     | **CF \_ OWNERDISPLAY**<br/> Wenn die Zwischenablage eines **CF \_ OWNERDISPLAY-Objekts** geleert wird, muss die Anwendung selbst das Speicherobjekt freigeben.<br/> |



 

 

