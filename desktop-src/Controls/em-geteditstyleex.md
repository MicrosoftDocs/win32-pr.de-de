---
title: EM_GETEDITSTYLEEX Meldung (RichEdit. h)
description: Ruft die aktuellen Flags für erweiterte Bearbeitungs Stile ab.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- Windows-Steuerelemente für EM_GETEDITSTYLEEX Meldung
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858950"
---
# <a name="em_geteditstyleex-message"></a>EM \_ geteditstyleex-Meldung

Ruft die aktuellen Flags für erweiterte Bearbeitungs Stile ab.


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die erweiterten Flags für den Bearbeitungs Stil zurück, die einen oder mehrere der folgenden Werte enthalten können.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ Ex- \_ handlerfriendlyurl**</dt> </dl>  | Anzeigen von anzeigen Amen mit derselben Textfarbe und Unterstreichung von automatischen Verknüpfungen, vorausgesetzt, dass die temporäre Formatierung nicht verwendet wurde oder die automatische Text Farbe verwendet (Standard: 0).<br/>                                                                       |
| <dl> <dt>**SES \_ Ex \_ multiberühren**</dt> </dl>         | Aktivieren Sie die Berührungs Unterstützung in Rich Edit. Dies schließt Auswahl, Caretzeichen und Kontextmenü Aufrufe ein. Wenn dieses Flag nicht festgelegt ist, wird die Fingereingabe durch Maus Befehle emuliert, die keine Besonderheiten im Touchscreen berücksichtigen (Standard: 0). <br/>      |
| <dl> <dt>**SES \_ Ex \_ noacetateselection**</dt> </dl> | Anzeigen von ausgewähltem Text mit klassischem Windows-Auswahl Text und Hintergrundfarben anstelle der Farbe für den Hintergrund (Standardwert: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ Ex \_ nomath**</dt> </dl>             | Einfügen von mathematischen Zonen deaktivieren (Standardwert: 1). Um die mathematische Bearbeitung und Anzeige zu aktivieren, senden Sie die Nachricht [**EM \_ seteditstyleex**](em-seteditstyleex.md) mit *wParam* auf 0 und *LPARAM* auf **SES \_ Ex \_ nomath**. <br/>                              |
| <dl> <dt>**wichtige SES-Werte \_ \_**</dt> </dl>            | Deaktivieren Sie das Einfügen von Tabellen. Die [**\_ geinsertfähige Nachricht "em insertting**](em-inserttable.md) " gibt " **E \_ Fail** " und RTF-Tabellen übersprungen (Standard: 0). <br/>                                                                                                  |
| <dl> <dt>**SES-Zeichen (USA) \_ \_**</dt> </dl>      | Aktivieren Sie ein mehrzeilige Steuerelement, das wie ein einzeilige Steuerelement ausgeführt werden kann, mit der Möglichkeit, vertikal scrollen, wenn die einzeilige Höhe größer als die Fensterhöhe ist (Standard: 0). <br/>                                                                   |
| <dl> <dt>**SES \_ hidetempformat**</dt> </dl>         | Blenden Sie die temporäre Formatierung aus, die erstellt wird, wenn " [**itextfont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) " mit **tomapplytmp** aufgerufen wird. Beispielsweise wird eine solche Formatierung von Rechtschreibprüfungen verwendet, um einen Wellen Strich unter Umständen falsch geschriebene Wörter anzuzeigen.<br/> |
| <dl> <dt>**SES \_ von \_ usemoust wParam**</dt> </dl>     | Verwenden Sie *wParam* , wenn Sie die [**WM- \_ mouanmove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht verarbeiten und [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)nicht aufrufen.<br/>                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ Test-ditstyleex**](em-seteditstyleex.md)
</dt> </dl>

 

