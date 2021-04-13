---
description: Das InkEdit-Steuerelement ist eine übergeordnete Klasse des RichEdit-Steuer Elements.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: InkEdit-Meldungen (nur Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b403e950ca67523620baab6f90a8fef9a47bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346119"
---
# <a name="inkedit-messages-win32-only"></a>InkEdit-Meldungen (nur Win32)

Das [InkEdit](inkedit-control-reference.md) -Steuerelement ist eine übergeordnete Klasse des [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) -Steuer Elements. Jede **RichEdit** -Nachricht wird direkt in den meisten Fällen an weitergeleitet und hat genau denselben Effekt wie in **RichEdit**. Dies gilt auch für Ereignis Benachrichtigungs Meldungen.

Um diese Nachrichten zu senden, wenden Sie die SendMessage-Funktion mit den folgenden Parametern an:



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>LRESULT SendMessage(
  HWND hWnd,      // handle to destination window
  UINT Msg,       // message
  WPARAM wParam,  // first message parameter
  LPARAM lParam   // second message parameter
);</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="message"></a>`Message`

Das übergeordnete Fenster des [InkEdit](inkedit-control-reference.md) -Steuer Elements empfängt Ereignis Benachrichtigungs Meldungen über die WM- \_ Benachrichtigungs Meldung:


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| Nachricht erhalten/festlegen                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EM \_ getinkmode<br/>           | Ruft den [inturingmodus des InkEdit](inkedit-control-reference.md) -Steuer Elements ab.<br/> Parameter:<br/> Diese Nachricht weist keine Parameter auf. *wParam* und *LPARAM* müssen den Wert 0 aufweisen.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der-Werte zurück, die in der [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) -Enumeration definiert sind. diese gibt an, ob die frei Hand Auflistung deaktiviert ist, ob frei Hand Eingaben gesammelt werden oder ob frei Hand Eingaben und Gesten gesammelt werden.<br/>                                                                                                                                                                                                                                                         |
| EM- \_ abkmode<br/>           | Legt den inkingmodus des [InkEdit](inkedit-control-reference.md) -Steuer Elements fest.<br/> Parameter:<br/>*wParam* Gibt einen der Werte der [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) -Enumeration an, der angibt, ob die frei Hand Auflistung deaktiviert ist, ob frei Hand Eingaben gesammelt werden oder ob frei Hand Eingaben und Gesten gesammelt werden.<br/>*LPARAM* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn der EM-GetStatus-Wert für " \_ IES im \_ Leerlauf"<br/>                                                                                                               |
| EM \_ getinkinsertmode<br/>     | Ruft den Freihand-Einfügemodus des [InkEdit](inkedit-control-reference.md) -Steuer Elements ab.<br/> Parameter:<br/> Diese Nachricht weist keine Parameter auf. *wParam* und *LPARAM* müssen den Wert 0 aufweisen.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der Werte der [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) -Enumeration zurück, der angibt, ob frei Hand Eingaben als Text oder als frei Handzeichen in das Steuerelement eingefügt werden.<br/>                                                                                                                                                                                                                                                                                                    |
| EM- \_ Objekt Modus<br/>     | Legt den Einfügemodus des [InkEdit](inkedit-control-reference.md) -Steuer Elements fest. Das Senden dieser Nachricht hat keine Auswirkung, wenn Sie mit einem anderen Betriebssystem als Microsoft Windows XP Tablet PC Edition verwendet wird.<br/> Parameter:<br/>*wParam* Gibt einen der Werte der [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) -Enumeration an, der angibt, ob frei Hand Eingaben als Text oder als frei Handzeichen in das Steuerelement eingefügt werden.<br/>*LPARAM* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                       |
| EM \_ getdrawattr<br/>          | Ruft die aktuellen Zeichnungs Attribute des [InkEdit](inkedit-control-reference.md) -Steuer Elements ab.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen Zeiger (iinkdrawingattributes \* \* pdrawattr) an, um das aktuelle [**inkdrawingattributes**](inkdrawingattributes-class.md) -Objekt zu empfangen.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                |
| EM \_ setdrawattr<br/>          | Legt die Zeichnungs Attribute fest, die für die zukünftige Freihand Auflistung verwendet werden.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen Zeiger (iinkdrawingattributes \* pdrawattr) an ein [**inkdrawingattributes**](inkdrawingattributes-class.md) -Objekt an.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                  |
| EM \_ getrecotimeout<br/>       | Ruft das Erkennungs Timeout in Millisekunden für das [InkEdit](inkedit-control-reference.md) -Steuerelement ab.<br/> Parameter:<br/> Diese Nachricht weist keine Parameter auf. *wParam* und *LPARAM* müssen den Wert 0 aufweisen.<br/> Rückgabewerte:<br/> Diese Meldung gibt das Erkennungs Timeout in Millisekunden zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| EM- \_ Start Timeout<br/>       | Legt das Erkennungs Timeout (in Millisekunden) für das [InkEdit](inkedit-control-reference.md) -Steuerelement fest.<br/> Parameter:<br/>*wParam* Gibt das Erkennungs Timeout in Millisekunden an.<br/>*LPARAM* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                                                    |
| EM \_ GetGestureStatus<br/>     | Ruft den Gesten Status für das [InkEdit](inkedit-control-reference.md) -Steuerelement ab.<br/> Parameter:<br/>*wParam* Gibt den Typ der Bewegung an, wie in der [**inkapplicationgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) -Enumeration definiert.<br/>*LPARAM* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt **true** zurück, wenn das [InkEdit](inkedit-control-reference.md) -Steuerelement die Bewegung abonniert hat, oder **false** , wenn das InkEdit-Steuerelement die Geste nicht abonniert.<br/>                                                                                                                                                                       |
| EM \_ SetGestureStatus<br/>     | Legt den Gesten Status für das [InkEdit](inkedit-control-reference.md) -Steuerelement fest.<br/> Parameter:<br/>*wParam* Gibt den Typ der Bewegung an, wie in der [**inkapplicationgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) -Enumeration definiert.<br/>*LPARAM* Gibt " **true** " an, wenn das Abonnieren der Geste aktiviert ist, oder " **false** ", wenn das lauschen an der Geste nicht aktiviert ist.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn der EM-GetStatus-Wert für " \_ IES im \_ Leerlauf"<br/>                                                                                                               |
| EM \_ getrecognizer<br/>        | Ruft die Erkennung ab, die vom [InkEdit](inkedit-control-reference.md) -Steuerelement verwendet wird.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen Zeiger auf einen iinkrecognizer \* an, um das [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt zu empfangen, das vom [InkEdit](inkedit-control-reference.md) -Steuerelement verwendet wird.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                   |
| EM-Ziel \_ Erkennungs Modul<br/>        | Legt die Erkennung fest, die vom [InkEdit](inkedit-control-reference.md) -Steuerelement verwendet wird. Wenn ein [Faktoid](factoid-constants.md) für das InkEdit-Steuerelement verwendet wird, muss es nach dem Senden dieser Nachricht erneut angewendet werden.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen Zeiger auf einen iinkrecognizer \* an, um das [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt festzulegen, das vom [InkEdit](inkedit-control-reference.md) -Steuerelement für die spätere Verwendung verwendet wird.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn der EM-GetStatus-Wert für " \_ IES im \_ Leerlauf"<br/> |
| EM \_ getfaktoid<br/>           | Ruft das für die Erkennung zu verwendende [Faktoid](factoid-constants.md) ab.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen Zeiger auf einen BSTR an, um die Faktoid-Zeichenfolge zu erhalten.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ setfatoid<br/>           | Legt das für die Erkennung zu verwendende [Faktoid](factoid-constants.md) fest.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt den BSTR-Wert an, der die Faktoid-Zeichenfolge enthält.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn der EM-GetStatus-Wert für " \_ IES im \_ Leerlauf"<br/>                                                                                                                                                                                                                                                                          |
| EM \_ getselink<br/>            | Ruft die frei Hand Eingaben innerhalb der Auswahl ab. Ink muss vor dem Zugriff über diese Nachricht erkannt werden. Wenn Sie nicht zuerst erkannt wird, \_ gibt EM getselink immer NULL [**InkDisp**](inkdisp-class.md) -Objekte zurück.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen Zeiger auf eine Variante an, um ein sicheres Array zum Empfangen von [**InkDisp**](inkdisp-class.md) -Objekten innerhalb der aktuellen Auswahl zu erhalten.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                     |
| EM \_ setselink<br/>            | Legt die frei Hand Eingaben innerhalb der Auswahl fest. Das Senden dieser Nachricht hat keine Auswirkung, wenn Sie mit einem anderen Betriebssystem als Windows XP Tablet PC Edition verwendet wird.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen Zeiger auf eine Variante mit einem sicheren Array von [**InkDisp**](inkdisp-class.md) -Objekten an, die die aktuelle Auswahl ersetzen sollen.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                     |
| EM \_ getselinkdisplaymode<br/> | Gibt die aktuelle Darstellung der frei Hand Eingabe im ausgewählten Bereich zurück, indem einer der Werte der [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) -Enumeration verwendet wird.<br/> Parameter:<br/> Diese Nachricht weist keine Parameter auf. *wParam* und *LPARAM* müssen den Wert 0 aufweisen.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der Werte der [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) -Enumeration (IDM \_ Text oder IDM \_ Ink) zurück, die angibt, wie eine Auswahl im Steuerelement angezeigt wird.<br/>                                                                                                                                                                                                                           |
| EM \_ setselinkdisplaymode<br/> | Legt die Darstellung der frei Hand Eingaben im ausgewählten Bereich fest, indem einer der Werte der [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) -Enumeration verwendet wird.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt an, wie Ink im ausgewählten Bereich angezeigt wird, wie in der [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) -Enumeration definiert.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt. Das Senden dieser Nachricht hat keine Auswirkung, wenn Sie mit einem anderen Betriebssystem als Windows XP Tablet PC Edition verwendet wird.<br/>                                                                                                   |
| EM \_ GetStatus<br/>            | Ruft den Status des [InkEdit](inkedit-control-reference.md) -Steuer Elements ab.<br/> Parameter:<br/> Diese Nachricht weist keine Parameter auf. *wParam* und *LPARAM* müssen den Wert 0 aufweisen.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der Werte der [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus) -Enumeration zurück, der angibt, ob sich das Steuerelement im Leerlauf befindet, frei Hand Eingaben sammelt oder frei Hand Eingaben erkennt.<br/>                                                                                                                                                                                                                                                                                                           |
| EM \_ erkennen<br/>            | Erzwingt die Erkennung.<br/> Parameter:<br/> Diese Nachricht weist keine Parameter auf. *wParam* und *LPARAM* müssen den Wert 0 aufweisen.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ getmouseicon<br/>         | Ruft das Maus Symbol ab.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Gibt einen HICON- \* Zeiger an, der mit dem aktuellen [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) -HICON ausgefüllt ist. Bei diesem HICON kann es sich entweder um einen HICON-oder einen **null** -Wert handeln.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                    |
| EM * \_ tmouseicon<br/>         | Legt das Maus Symbol fest.<br/> Parameter:<br/>*wParam* Gibt einen booleschen Wert an, der auf **true** festgelegt wird, wenn das [InkEdit](inkedit-control-reference.md) -Steuerelement den HICON-Handle besitzen soll, oder **false** , wenn das InkEdit-Steuerelement den HICON-Handle nicht besitzen soll. Wenn das InkEdit-Steuerelement das HICON besitzt, wird das HICON entsprechend übernommen und zerstört. Andernfalls besitzt der Aufrufer das HICON und ist dafür verantwortlich, ihn zu löschen.<br/>*LPARAM* Gibt den neuen HICON-Wert an. Verwenden Sie **null** , um den Wert zu löschen. Der Standardwert ist **NULL**.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                |
| EM \_ getmoucpointer<br/>      | Ruft den Mauszeiger ab.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Enthält einen inkmouspointer- \* Zeiger, der mit dem aktuellen [**mouspointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) -Wert aufgefüllt wird. Dies verhält sich wie die Eigenschaft **InkCollector:: get \_ mougenpointer** .<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                            |
| EM \_ -Timeout<br/>      | Legt den Mauszeiger fest.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/>*LPARAM* Enthält den neuen [**mouspointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) -Wert, der in der [**inkmouspointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) -Enumeration definiert ist. Dies verhält sich wie die Eigenschaft **InkCollector::p UT \_ mougenpointer** .<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                    |
| EM \_ getusemouseforinput<br/>  | Ruft den Zustand ab, ob Maus Eingaben als Stift Eingaben behandelt werden.<br/> Parameter:<br/> Diese Nachricht weist keine Parameter auf. *wParam* und *LPARAM* müssen den Wert 0 aufweisen.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn **false** oder 1, wenn **true**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ setusemouseforinput<br/>  | Legt den Status fest, der angibt, ob Maus Eingaben als Stift Eingaben behandelt werden.<br/> Parameter:<br/>*wParam* Gibt einen booleschen Wert an, der bestimmt, ob die Mauseingabe als Stift Eingabe behandelt werden soll.<br/>*LPARAM* Dieser Parameter wird nicht verwendet. der Wert muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt bei Erfolg 0 (null) zurück, wenn ein Fehler auftritt.<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn der EM-GetStatus-Wert für " \_ IES im \_ Leerlauf"<br/>                                                                                                                                                                                                                                             |



 



| Ereignis Benachrichtigungs Meldung         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IECN- \_ Strich<br/>            | Benachrichtigt das übergeordnete Fenster des [InkEdit](inkedit-control-reference.md) -Steuer Elements, dass ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) erstellt wurde. Dies wird in einer WM- \_ Benachrichtigungs Meldung mit den folgenden Parametern gesendet.<br/> Parameter:<br/>*wParam* Gibt den Bezeichner des Steuer Elements an, das die Nachricht gesendet hat.<br/>*LPARAM* Gibt einen Zeiger auf die [**IEC \_ strokeinfo**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo) -Struktur an.<br/> Rückgabewerte:<br/> Der Client gibt 0 zurück, um den Strich zu akzeptieren, und 1, um den Strich abzubrechen.<br/> |
| IECN- \_ Geste<br/>           | Benachrichtigt das übergeordnete Fenster des [InkEdit](inkedit-control-reference.md) -Steuer Elements, dass eine Geste erkannt wurde. Dies wird in einer WM- \_ Benachrichtigungs Meldung mit den folgenden Parametern gesendet.<br/> Parameter:<br/>*wParam* Gibt den Bezeichner des Steuer Elements an, das die Nachricht gesendet hat.<br/>*LPARAM* Gibt einen Zeiger auf die [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo) -Struktur an.<br/> Rückgabewerte:<br/> Der Client gibt 0 zurück, um die Geste zu akzeptieren, und 1, um die Geste abzubrechen.<br/>                           |
| IECN- \_ Erkennungs Ergebnis<br/> | Benachrichtigt das übergeordnete Fenster des [InkEdit](inkedit-control-reference.md) -Steuer Elements, dass eine Erkennung aufgetreten ist. Dies wird in einer WM- \_ Benachrichtigungs Meldung mit den folgenden Parametern gesendet.<br/> Parameter:<br/>*wParam* Gibt den Bezeichner des Steuer Elements an, das die Nachricht gesendet hat.<br/>*LPARAM* Gibt einen Zeiger auf die [**IEC- \_ erkennungsresultinfo**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) -Struktur an.<br/> Rückgabewerte:<br/> Der Client gibt 0 zurück, wenn die Nachricht verarbeitet wird.<br/>                                  |



 

## <a name="applies-to"></a>Gilt für

-   [InkEdit](inkedit-control-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IEC \_ GESTUREINFO-Struktur (nur Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**IEC \_ strokeinfo-Struktur (nur Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**IEC- \_ erkennungsresultinfo-Struktur (nur Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**Mougenpointer (Eigenschaft)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**InkEditStatus-Enumeration**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**InkInsertMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**InkMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Inkdrawingattributes-Klasse**](inkdrawingattributes-class.md)
</dt> <dt>

[**Iinkrecognitionresult-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**Iinkrecognizer-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**Iinkgesten-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

