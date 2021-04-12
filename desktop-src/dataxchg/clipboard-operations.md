---
title: Zwischenablage Vorgänge
description: Ein Fenster sollte die Zwischenablage beim Ausschnitten, kopieren oder Einfügen von Daten verwenden. Ein Fenster platziert Daten für Ausschneide-und Kopiervorgänge in der Zwischenablage und ruft Daten für Einfügevorgänge aus der Zwischenablage ab.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Windows-Benutzeroberfläche, Zwischenablage
- Zwischenablage, Fenster
- Zwischenablage, Daten werden abgeschnitten
- Zwischenablage, Kopieren von Daten
- Zwischenablage, Einfügen von Daten
- Zwischenablage, Besitzer Fenster
- Zwischenablage, verzögertes Rendering
- Zwischenablage, Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb2c3451cf562b35b976e137a974e19892acbb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316214"
---
# <a name="clipboard-operations"></a>Zwischenablage Vorgänge

Ein Fenster sollte die Zwischenablage beim Ausschnitten, kopieren oder Einfügen von Daten verwenden. Ein Fenster platziert Daten für Ausschneide-und Kopiervorgänge in der Zwischenablage und ruft Daten für Einfügevorgänge aus der Zwischenablage ab. In den folgenden Abschnitten werden diese Vorgänge und zugehörigen Probleme beschrieben.

Zum Platzieren von Daten oder zum Abrufen von Daten aus der Zwischenablage muss ein Fenster die Zwischenablage zunächst mithilfe der [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) -Funktion öffnen. Nur in einem Fenster kann die Zwischenablage gleichzeitig geöffnet sein. Um herauszufinden, in welchem Fenster die Zwischenablage geöffnet ist, können Sie die [**getopenclipboardwindow**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) -Funktion aufrufen. Nachdem der Vorgang abgeschlossen ist, muss das Fenster die Zwischenablage schließen, indem die [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) -Funktion aufgerufen wird.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Ausschneide-und Kopiervorgänge](#cut-and-copy-operations)
-   [Einfügevorgänge](#paste-operations)
-   [Besitz der Zwischenablage](#clipboard-ownership)
-   [Verzögertes Rendering](#delayed-rendering)
-   [Arbeitsspeicher und Zwischenablage](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Ausschneide-und Kopiervorgänge

Zum Platzieren von Informationen in der Zwischenablage löscht ein Fenster zuerst den vorherigen Inhalt der Zwischenablage mithilfe der [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) -Funktion. Diese Funktion sendet die [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht an den vorherigen Besitzer der Zwischenablage, gibt Ressourcen frei, die Daten in der Zwischenablage zugeordnet sind, und weist den Zwischenablage Besitz dem Fenster zu, in dem die Zwischenablage geöffnet ist. Um herauszufinden, welches Fenster die Zwischenablage besitzt, können Sie die [**getclipboardowner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) -Funktion aufrufen.

Nach dem leeren der Zwischenablage platziert das Fenster Daten in der Zwischenablage in so vielen Zwischenablage Formaten wie möglich, geordnet nach dem am besten beschreibenden Zwischenablage Format. Für jedes Format Ruft das Fenster die [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) -Funktion auf und gibt den Format Bezeichner und ein globales Speicher Handle an. Das Speicher Handle kann NULL sein, was bedeutet, dass das Fenster die Daten bei der Anforderung rendert. Weitere Informationen finden Sie unter [Verzögertes Rendering](#delayed-rendering).

## <a name="paste-operations"></a>Einfügevorgänge

Um Einfüge Informationen aus der Zwischenablage abzurufen, bestimmt ein Fenster zuerst das abzurufende Zwischenablage Format. In der Regel listet ein Fenster die verfügbaren Zwischenablage Formate mithilfe der [**enumclipboardformats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) -Funktion auf und verwendet das erste Format, das es erkennt. Diese Methode wählt das beste verfügbare Format gemäß dem Prioritäts Satz aus, wenn die Daten in der Zwischenablage platziert wurden.

Alternativ kann ein Fenster die [**getpriorityclipboardformat**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) -Funktion verwenden. Diese Funktion identifiziert das beste verfügbare Zwischenablage Format entsprechend einer angegebenen Priorität. Ein Fenster, das nur ein Zwischenablage Format erkennt, kann einfach bestimmen, ob dieses Format mithilfe der [**isclipboardformatavailable**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable) -Funktion verfügbar ist.

Nachdem Sie das zu verwendende Zwischenablage Format festgelegt haben, Ruft ein Fenster die [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) -Funktion auf. Diese Funktion gibt das Handle für ein globales Speicher Objekt zurück, das Daten im angegebenen Format enthält. Ein Fenster kann das Speicher Objekt kurz sperren, um die Daten zu überprüfen oder zu kopieren. Ein Fenster sollte das Objekt jedoch nicht freigeben oder für einen längeren Zeitraum gesperrt bleiben.

## <a name="clipboard-ownership"></a>Besitz der Zwischenablage

Der *Besitzer der Zwischenablage* ist das Fenster, das den Informationen in der Zwischenablage zugeordnet ist. Ein Fenster wird zum Besitzer der Zwischenablage, wenn Daten in der Zwischenablage platziert werden, insbesondere wenn die [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) -Funktion aufgerufen wird. Das Fenster bleibt der Besitzer der Zwischenablage, bis es geschlossen wird oder ein anderes Fenster die Zwischenablage leert.

Wenn die Zwischenablage geleert wird, empfängt der Besitzer der Zwischenablage eine [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht. Es folgen einige Gründe, warum ein Fenster diese Nachricht verarbeiten kann:

-   Das Fenster verzögerte Rendering von einem oder mehreren Zwischenablage Formaten. Als Antwort auf die Meldung " [**WM \_ destroyclipboard**](wm-destroyclipboard.md) " gibt das Fenster möglicherweise Ressourcen frei, die ihm zugeordnet wurden, um Daten auf Anforderung zu Rendering. Weitere Informationen zum Rendern von Daten finden Sie unter [Verzögertes Rendering](#delayed-rendering).
-   Das Fenster hat Daten in der Zwischenablage in einem privaten Zwischenablage Format abgelegt. Die Daten für private Zwischenablage Formate werden vom System nicht freigegeben, wenn die Zwischenablage geleert wird. Daher sollte der Besitzer der Zwischenablage die Daten beim Empfang der [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht freigeben. Weitere Informationen zu privaten Zwischenablage Formaten finden Sie unter [Zwischenablage Formate](clipboard-formats.md).
-   Das Fenster hat Daten in der Zwischenablage mithilfe des CF-Besitzer **\_ Anzeige** -Zwischenablage Formats platziert. Als Antwort auf die [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht gibt das Fenster möglicherweise Ressourcen frei, die für die Anzeige von Informationen im Fenster der Zwischenablage Anzeige verwendet wurden. Weitere Informationen zu diesem alternativen Format finden Sie unter [Anzeige Format des Besitzers](about-the-clipboard.md).

## <a name="delayed-rendering"></a>Verzögertes Rendering

Wenn Sie ein Zwischenablage Format in der Zwischenablage platzieren, kann ein Fenster das Rendern der Daten in diesem Format verzögern, bis die Daten benötigt werden. Zu diesem Zweck kann eine Anwendung **null** für den *hdata* -Parameter der [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) -Funktion angeben. Dies ist hilfreich, wenn die Anwendung mehrere Zwischenablage Formate unterstützt, von denen einige oder alle zeitaufwändig zum Renderingformat sind. Durch die Übergabe eines **null** -Handles rendert ein Fenster komplexe Zwischenablage Formate nur dann, wenn Sie benötigt werden.

Wenn ein Fenster das Rendern eines Zwischenablage Formats verzögert, muss es darauf vorbereitet sein, das Format auf Anforderung zu rendern, solange es der Besitzer der Zwischenablage ist. Das System sendet dem Besitzer der Zwischenablage eine [**WM- \_ Renderformat**](wm-renderformat.md) -Nachricht, wenn eine Anforderung für ein bestimmtes Format empfangen wird, das nicht gerendert wurde. Beim Empfang dieser Nachricht sollte das Fenster die [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) -Funktion aufrufen, um ein globales Speicher Handle in der Zwischenablage im angeforderten Format zu platzieren.

Eine Anwendung darf die Zwischenablage vor dem Aufruf von [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) nicht als Antwort auf die [**WM- \_ Renderformat**](wm-renderformat.md) -Meldung öffnen. Das Öffnen der Zwischenablage ist nicht erforderlich, und jeder Versuch, dies zu tun, schlägt fehl, da die Zwischenablage derzeit von der Anwendung geöffnet wird, die das Rendern des Formats angefordert hat.

Wenn der Besitzer der Zwischenablage zerstört wird und einige oder alle Zwischenablage Formate verzögert rendern, empfängt er die [**WM- \_ renderallformats**](wm-renderallformats.md) -Nachricht. Beim Empfang dieser Nachricht sollte das Fenster die Zwischenablage öffnen, überprüfen, ob es weiterhin der Besitzer der Zwischenablage mit der [**getclipboardowner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) -Funktion ist, und dann gültige Speicher Handles für alle Zwischenablage Formate in der Zwischenablage platzieren. Dadurch wird sichergestellt, dass diese Formate verfügbar bleiben, nachdem der Besitzer der Zwischenablage zerstört wurde.

Anders als bei [**WM \_ Renderformat**](wm-renderformat.md)sollte eine Anwendung, die auf [**WM \_ renderallformats**](wm-renderallformats.md) antwortet, die Zwischenablage öffnen, bevor [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) aufgerufen wird, um globale Speicher Handles in der Zwischenablage zu platzieren.

Alle Zwischenablage Formate, die nicht als Antwort auf die [**WM- \_ renderallformats**](wm-renderallformats.md) -Nachricht gerendert werden, sind für andere Anwendungen nicht mehr verfügbar und werden nicht mehr durch die Zwischenablage Funktionen aufgelistet.

## <a name="memory-and-the-clipboard"></a>Arbeitsspeicher und Zwischenablage

Ein Speicher Objekt, das in der Zwischenablage platziert werden soll, muss mithilfe der [**globalzuzuordnungs**](/windows/desktop/api/winbase/nf-winbase-globalalloc) -Funktion mit dem für **GMEM Verschieb \_ baren** Flag zugewiesen werden.

Nachdem ein Speicher Objekt in der Zwischenablage abgelegt wurde, wird der Besitz dieses Speicher Handles an das System übertragen. Wenn die Zwischenablage geleert wird und das Speicher Objekt eines der folgenden Zwischenablage Formate aufweist, gibt das System das Speicher Objekt frei, indem die angegebene Funktion aufgerufen wird:



| Funktion zum freien Objekt                             | Zwischenablage Format                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ dspenhmetafile**<br/> **CF \_ dspmetafilepict**<br/> **CF \_ enhmetafile**<br/> **CF- \_ MetafilePict**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **CF- \_ Bitmap**<br/> **CF- \_ dspbitmap**<br/> **CF- \_ Palette**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **CF- \_ DIB**<br/> **CF \_ DIBV5**<br/> **CF- \_ dsptext**<br/> **CF- \_ OemText**<br/> **CF- \_ Text**<br/> **CF \_ UnicodeText**<br/>   |
| none<br/>                                     | **CF-Besitzer \_ Anzeige**<br/> Wenn die Zwischenablage von einem CF-Besitzer **\_ Anzeige** Objekt geleert wird, muss die Anwendung selbst das Speicher Objekt freigeben.<br/> |



 

 

