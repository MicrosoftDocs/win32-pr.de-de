---
description: Das InkEdit-Steuerelement ist eine Superklasse des RichEdit-Steuerelements.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: InkEdit Messages (Nur Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cb1d390bf8e37d6affbbd96c34c53ea889b268
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475036"
---
# <a name="inkedit-messages-win32-only"></a>InkEdit Messages (Nur Win32)

Das [InkEdit-Steuerelement](inkedit-control-reference.md) ist eine Superklasse des [**RichEdit-Steuerelements.**](/windows/desktop/api/richole/nn-richole-iricheditole) Jede **RichEdit-Nachricht** wird in den meisten Fällen direkt übergeben und hat genau die gleiche Auswirkung wie in **RichEdit.** Dies gilt auch für Ereignisbenachrichtigungen.

Um diese Nachrichten zu senden, rufen Sie die SendMessage-Funktion mit den folgenden Parametern auf:




| C++ | 
|-----|
| <pre data-space="preserve"><code>LRESULT SendMessage(  HWND hWnd,      // handle to destination window  UINT Msg,       // message  WPARAM wParam,  // first message parameter  LPARAM lParam   // second message parameter);</code></pre> | 




 

## <a name="message"></a>`Message`

Das übergeordnete Fenster des [InkEdit-Steuerelements](inkedit-control-reference.md) empfängt Ereignisbenachrichtigungsmeldungen über die WM \_ NOTIFY-Nachricht:


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| Get/set message (Nachricht abrufen/festlegen)                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EM \_ GETINKMODE<br/>           | Ruft den [InkEdit-Modus des InkEdit-Steuerelements](inkedit-control-reference.md) ab.<br/> Parameter:<br/> Diese Nachricht enthält keine Parameter. *wParam* und *lParam* müssen 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der Werte zurück, die in der [**InkMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkmode) definiert sind, der angibt, ob die Ink-Sammlung deaktiviert ist, ob Ink gesammelt wird oder ob Ink- und Gesten gesammelt werden.<br/>                                                                                                                                                                                                                                                         |
| EM \_ SETINKMODE<br/>           | Legt den InkEdit-Modus des [InkEdit-Steuerelements](inkedit-control-reference.md) fest.<br/> Parameter:<br/>*wParam* Gibt einen der Werte der [**InkMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkmode) an, der angibt, ob die Ink-Sammlung deaktiviert ist, ob Ink gesammelt wird oder ob Ink- und Gesten gesammelt werden.<br/>*lParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn DER EM \_ GETSTATUS IES \_ Idle zurückgibt.<br/>                                                                                                               |
| EM \_ GETINKINSERTMODE<br/>     | Ruft den Ink-Einfügemodus des [InkEdit-Steuerelements](inkedit-control-reference.md) ab.<br/> Parameter:<br/> Diese Nachricht enthält keine Parameter. *wParam* und *lParam* müssen 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der Werte der [**InkInsertMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkinsertmode) zurück, der angibt, ob Ink als Text oder als Ink in das Steuerelement eingefügt wird.<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETINKINSERTMODE<br/>     | Legt den Ink-Einfügemodus des [InkEdit-Steuerelements](inkedit-control-reference.md) fest. Das Senden dieser Nachricht hat keine Auswirkungen, wenn es mit einem anderen Betriebssystem als Microsoft Windows XP Tablet PC Edition verwendet wird.<br/> Parameter:<br/>*wParam* Gibt einen der Werte der [**InkInsertMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkinsertmode) an, der angibt, ob Ink als Text oder als Ink in das Steuerelement eingefügt wird.<br/>*lParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/>                                                                                                       |
| EM \_ GETDRAWATTR<br/>          | Ruft die aktuellen Zeichnungsattribute des [InkEdit-Steuerelements](inkedit-control-reference.md) ab.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen Zeiger (IInkDrawingAttributes \* \* pDrawAttr) zum Empfangen des aktuellen [**InkDrawingAttributes-Objekts**](inkdrawingattributes-class.md) an.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/>                                                                                                                                                                                                                                                |
| EM \_ SETDRAWATTR<br/>          | Legt die Zeichnungsattribute fest, die für die zukünftige Ink-Auflistung verwendet werden sollen.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen Zeiger (IInkDrawingAttributes \* pDrawAttr) auf ein [**InkDrawingAttributes-Objekt**](inkdrawingattributes-class.md) an.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/>                                                                                                                                                                                                                                                                                                  |
| EM \_ GETRECOTIMEOUT<br/>       | Ruft das Erkennungstimeout für das [InkEdit-Steuerelement](inkedit-control-reference.md) in Millisekunden ab.<br/> Parameter:<br/> Diese Nachricht enthält keine Parameter. *wParam* und *lParam* müssen 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt das Erkennungstimeout in Millisekunden zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ SETRECOTIMEOUT<br/>       | Legt das Erkennungstimeout für das [InkEdit-Steuerelement](inkedit-control-reference.md) in Millisekunden fest.<br/> Parameter:<br/>*wParam* Gibt das Erkennungstimeout in Millisekunden an.<br/>*lParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/>                                                                                                                                                                                                                                                                                                                                    |
| EM \_ GETGESTURESTATUS<br/>     | Ruft den Gestenstatus für das [InkEdit-Steuerelement](inkedit-control-reference.md) ab.<br/> Parameter:<br/>*wParam* Gibt den Typ der Geste an, wie in der [**InkApplicationGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) definiert.<br/>*lParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt **TRUE** zurück, wenn das [InkEdit-Steuerelement](inkedit-control-reference.md) die Geste abonniert, oder **FALSE,** wenn das InkEdit-Steuerelement die Geste nicht abonniert.<br/>                                                                                                                                                                       |
| EM \_ SETGESTURESTATUS<br/>     | Legt den Gestenstatus für das [InkEdit-Steuerelement](inkedit-control-reference.md) fest.<br/> Parameter:<br/>*wParam* Gibt den Typ der Geste an, wie in der [**InkApplicationGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) definiert.<br/>*lParam* Gibt **TRUE** an, wenn das Abonnieren der Geste aktiviert ist, oder **FALSE,** wenn das Lauschen auf die Geste nicht aktiviert ist.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn DER EM \_ GETSTATUS IES \_ Idle zurückgibt.<br/>                                                                                                               |
| EM \_ GETRECOGNIZER<br/>        | Ruft die Erkennung ab, die vom [InkEdit-Steuerelement](inkedit-control-reference.md) verwendet wird.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen Zeiger auf einen IInkRecognizer \* an, um das [**IInkRecognizer-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) zu empfangen, das vom [InkEdit-Steuerelement](inkedit-control-reference.md) verwendet wird.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/>                                                                                                                                                                                                                                   |
| EM \_ SETRECOGNIZER<br/>        | Legt die Erkennung fest, die vom [InkEdit-Steuerelement](inkedit-control-reference.md) verwendet wird. Wenn ein [Factoid](factoid-constants.md) für das InkEdit-Steuerelement verwendet wird, muss es nach dem Senden dieser Nachricht erneut angewendet werden.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen Zeiger auf einen IInkRecognizer \* an, um das [**IInkRecognizer-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) festzulegen, das das [InkEdit-Steuerelement](inkedit-control-reference.md) für die spätere Verwendung verwendet.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn EM \_ GETSTATUS IES \_ Idle zurückgibt.<br/> |
| EM \_ GETFACTOID<br/>           | Ruft das [Factoid ab,](factoid-constants.md) das für die Erkennung verwendet werden soll.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen Zeiger auf einen BSTR an, um die Faktenzeichenfolge zu empfangen.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETFACTOID<br/>           | Legt das [Factoid fest,](factoid-constants.md) das für die Erkennung verwendet werden soll.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt den BSTR an, der die Faktenzeichenfolge enthält.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn EM \_ GETSTATUS IES \_ Idle zurückgibt.<br/>                                                                                                                                                                                                                                                                          |
| EM \_ GETSELINK<br/>            | Ruft die Ink-Datei innerhalb der Auswahl ab. Ink muss erkannt werden, bevor über diese Nachricht auf zugegriffen wird. Wenn er nicht zuerst erkannt wird, gibt EM \_ GETSELINK immer null [**InkDisp-Objekte**](inkdisp-class.md) zurück.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen Zeiger auf eine VARIANT an, um ein sicheres Array zum Empfangen von [**InkDisp-Objekten innerhalb**](inkdisp-class.md) der aktuellen Auswahl zu empfangen.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                                                                                                                     |
| EM \_ SETSELINK<br/>            | Legt die Ink-Datei innerhalb der Auswahl fest. Das Senden dieser Meldung hat keine Auswirkungen, wenn es mit einem betriebssystem installierten anderen Betriebssystem als Windows XP Tablet PC Edition verwendet wird.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen Zeiger auf eine VARIANT-Datei mit einem sicheren Array von [**InkDisp-Objekten**](inkdisp-class.md) an, um die aktuelle Auswahl zu ersetzen.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                     |
| EM \_ GETSELINKDISPLAYMODE<br/> | Gibt die aktuelle Darstellung der Ink-Funktion im ausgewählten Bereich zurück, indem einer der Werte der [**InkDisplayMode-Enumeration verwendet**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) wird.<br/> Parameter:<br/> Diese Meldung verfügt über keine Parameter. *wParam* und *lParam* müssen 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der Werte der [**InkDisplayMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (IDM-Text oder \_ IDM-Ink) zurück, der angibt, wie eine Auswahl auf dem \_ Steuerelement angezeigt wird.<br/>                                                                                                                                                                                                                           |
| EM \_ SETSELINKDISPLAYMODE<br/> | Legt die Darstellung der InkDisplayMode-Enumeration im ausgewählten Bereich mithilfe eines der Werte der [**InkDisplayMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) fest.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt an, wie Ink Im ausgewählten Bereich angezeigt wird, wie in der [**InkDisplayMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) definiert.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt. Das Senden dieser Meldung hat keine Auswirkungen, wenn es mit einem betriebssystem installierten anderen Betriebssystem als Windows XP Tablet PC Edition verwendet wird.<br/>                                                                                                   |
| EM \_ GETSTATUS<br/>            | Ruft den Status des [InkEdit-Steuerelements](inkedit-control-reference.md) ab.<br/> Parameter:<br/> Diese Meldung verfügt über keine Parameter. *wParam* und *lParam* müssen 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt einen der Werte der [**InkEditStatus-Enumeration**](/windows/desktop/api/inked/ne-inked-inkeditstatus) zurück, der angibt, ob sich das Steuerelement im Leerlauf befindet, Ink sammelt oder Ink erkennt.<br/>                                                                                                                                                                                                                                                                                                           |
| EM \_ RECOGNIZE<br/>            | Erzwingt die Erkennung.<br/> Parameter:<br/> Diese Meldung verfügt über keine Parameter. *wParam* und *lParam* müssen 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ GETMOUSEICON<br/>         | Ruft das Maussymbol ab.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Gibt einen HICON-Zeiger an, der mit dem aktuellen \* [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) HICON aufgefüllt wird. Diese HICON kann entweder ein HICON- oder ein **NULL-Wert** sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETMOUSEICON<br/>         | Legt das Maussymbol fest.<br/> Parameter:<br/>*wParam* Gibt einen BOOLESCHEN Wert an, der auf **TRUE** festgelegt ist, wenn das [InkEdit-Steuerelement](inkedit-control-reference.md) das HICON-Handle besitzen soll, oder **FALSE,** wenn das InkEdit-Steuerelement nicht das HICON-Handle besitzen soll. Wenn das InkEdit-Steuerelement den HICON besitzt, übernimmt es das HICON und zerstört es entsprechend. Andernfalls besitzt der Aufrufer den HICON und ist für das Löschen verantwortlich.<br/>*lParam* Gibt den neuen HICON-Wert an. Verwenden **Sie NULL,** um den Wert zu löschen. Der Standardwert ist **NULL**.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                |
| EM \_ GETMOUSEPOINTER<br/>      | Ruft den Mauszeiger ab.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Enthält einen InkMousePointer-Zeiger, der mit dem \* aktuellen [**MousePointer-Wert gefüllt**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) ist. Dies verhält sich genauso wie die **InkCollector::get \_ MousePointer-Eigenschaft.**<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                                            |
| EM \_ SETMOUSEPOINTER<br/>      | Legt den Mauszeiger fest.<br/> Parameter:<br/>*wParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/>*lParam* Enthält den neuen [**MousePointer-Wert,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) der in der [**InkMousePointer-Enumeration definiert**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) ist. Dies verhält sich genauso wie die **InkCollector::p ut \_ MousePointer-Eigenschaft.**<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 zurück, wenn erfolgreich oder ungleich 0 (null), wenn ein Fehler auftritt.<br/>                                                                                                                                                                                                                                    |
| EM \_ GETUSEMOUSEFORINPUT<br/>  | Ruft den Status ab, ob Mauseingaben als Stifteingabe behandelt werden.<br/> Parameter:<br/> Diese Meldung verfügt über keine Parameter. *wParam* und *lParam* müssen 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 bei **FALSE** oder 1 bei **TRUE** zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETUSEMOUSEFORINPUT<br/>  | Legt den Zustand fest, ob die Mauseingabe als Stifteingabe behandelt wird.<br/> Parameter:<br/>*wParam* Gibt einen booleschen Wert an, der bestimmt, ob Mauseingaben als Stifteingabe behandelt werden sollen.<br/>*lParam* Dieser Parameter wird nicht verwendet. muss 0 sein.<br/> Rückgabewerte:<br/> Diese Meldung gibt 0 (null) zurück, wenn der Fehler erfolgreich ist, oder bei einem Fehler ungleich 0 (null).<br/> Anmerkungen:<br/> Dies sollte nur verwendet werden, wenn DER EM \_ GETSTATUS IES \_ Idle zurückgibt.<br/>                                                                                                                                                                                                                                             |



 



| Ereignisbenachrichtigungsmeldung         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IECN \_ STROKE<br/>            | Benachrichtigt das übergeordnete Fenster des [InkEdit-Steuerelements,](inkedit-control-reference.md) dass ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) erstellt wurde. Dies wird in einer WM \_ NOTIFY-Nachricht mit den folgenden Parametern gesendet.<br/> Parameter:<br/>*wParam* Gibt den Bezeichner des Steuerelements an, das die Nachricht gesendet hat.<br/>*lParam* Gibt einen Zeiger auf die [**IEC \_ STROKEINFO-Struktur**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo) an.<br/> Rückgabewerte:<br/> Der Client gibt 0 zurück, um den Strich zu akzeptieren, und 1, um den Strich abzubrechen.<br/> |
| \_IECN-GESTE<br/>           | Benachrichtigt das übergeordnete Fenster des [InkEdit-Steuerelements,](inkedit-control-reference.md) dass eine Geste erkannt wurde. Dies wird in einer WM \_ NOTIFY-Nachricht mit den folgenden Parametern gesendet.<br/> Parameter:<br/>*wParam* Gibt den Bezeichner des Steuerelements an, das die Nachricht gesendet hat.<br/>*lParam* Gibt einen Zeiger auf die [**IEC \_ GESTUREINFO-Struktur**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo) an.<br/> Rückgabewerte:<br/> Der Client gibt 0 zurück, um die Geste zu akzeptieren, und 1, um die Geste abzubrechen.<br/>                           |
| IECN \_ RECOGNITIONRESULT<br/> | Benachrichtigt das übergeordnete Fenster des [InkEdit-Steuerelements,](inkedit-control-reference.md) dass eine Erkennung aufgetreten ist. Dies wird in einer WM \_ NOTIFY-Nachricht mit den folgenden Parametern gesendet.<br/> Parameter:<br/>*wParam* Gibt den Bezeichner des Steuerelements an, das die Nachricht gesendet hat.<br/>*lParam* Gibt einen Zeiger auf die [**IEC \_ RECOGNITIONRESULTINFO-Struktur**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) an.<br/> Rückgabewerte:<br/> Der Client gibt 0 zurück, wenn er die Nachricht verarbeitet.<br/>                                  |



 

## <a name="applies-to"></a>Gilt für

-   [Inkedit](inkedit-control-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IEC \_ GESTUREINFO-Struktur (nur Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**IEC \_ STROKEINFO-Struktur (nur Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**IEC \_ RECOGNITIONRESULTINFO-Struktur (nur Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**MousePointer-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**InkEditStatus-Enumeration**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**InkInsertMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**InkMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDrawingAttributes-Klasse**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkRecognitionResult-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**IInkRecognizer-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**IInkGesture-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

