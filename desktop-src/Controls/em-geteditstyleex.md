---
title: EM_GETEDITSTYLEEX (Richedit.h)
description: Ruft die aktuellen erweiterten Bearbeitungsstilflags ab.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX der Windows Steuerelemente
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
ms.openlocfilehash: ad3c011a162bbf0a1822e68be6bd60f662551b3a22ecfca62c64ef8d01a605a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049310"
---
# <a name="em_geteditstyleex-message"></a>EM \_ GETEDITSTYLEEX-Nachricht

Ruft die aktuellen erweiterten Bearbeitungsstilflags ab.


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

Gibt die erweiterten Bearbeitungsstilflags zurück, die einen oder mehrere der folgenden Werte enthalten können.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ EX \_ HANDLEFRIENDLYURL**</dt> </dl>  | Anzeigen von Anzeigenamenlinks mit der gleichen Textfarbe und Gliederung wie automatische Links, vorausgesetzt, die temporäre Formatierung wird nicht verwendet oder verwendet text autocolor (Standard: 0).<br/>                                                                       |
| <dl> <dt>**SES \_ EX \_ MULTITOUCH**</dt> </dl>         | Aktivieren Sie die Touchunterstützung in Rich Edit. Dies schließt Auswahl, Ein caretplatzierung und Kontextmenüaufrufe ein. Wenn dieses Flag nicht festgelegt ist, wird die Fingerbewegung durch Mausbefehle emuliert, die keine Besonderheiten des Touchmodus berücksichtigen (Standardeinstellung: 0). <br/>      |
| <dl> <dt>**SES \_ EX \_ NOACETATESELECTION**</dt> </dl> | Anzeigen von ausgewähltem Text mit Windows Auswahltext und Hintergrundfarben anstelle der Hintergrund acetate-Farbe (Standardeinstellung: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ EX \_ NOMATH**</dt> </dl>             | Deaktivieren Sie das Einfügen von mathematischen Zonen (Standard: 1). Um die mathematische Bearbeitung und Anzeige zu aktivieren, senden Sie die [**EM \_ SETEDITSTYLEEX-Nachricht,**](em-seteditstyleex.md) bei der *wParam* auf 0 und *lParam* auf **SES \_ EX \_ NOMATH festgelegt ist.** <br/>                              |
| <dl> <dt>**SES \_ EX \_ NOTABLE**</dt> </dl>            | Deaktivieren Sie das Einfügen von Tabellen. Die [**EM \_ INSERTTABLE-Meldung**](em-inserttable.md) gibt **E FAIL \_ zurück,** und RTF-Tabellen werden übersprungen (Standard: 0). <br/>                                                                                                  |
| <dl> <dt>**SES \_ EX \_ VERWENDETINGLELINE**</dt> </dl>      | Aktivieren Sie ein mehrzeilenbasiertes Steuerelement, das wie ein einzeilenbasiertes Steuerelement mit der Möglichkeit, vertikal zu scrollen, wenn die Einzeilenhöhe größer als die Fensterhöhe ist (Standard: 0). <br/>                                                                   |
| <dl> <dt>**SES \_ HIDETEMPFORMAT**</dt> </dl>         | Blenden Sie die temporäre Formatierung aus, die erstellt wird, wenn [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) mit **tomApplyTmp aufgerufen wird.** Eine solche Formatierung wird z. B. von Rechtschreibprüfungsoptionen verwendet, um unter möglicherweise falsch geschriebenen Wörtern eine gestrichelte Unterstreichung anzuzeigen.<br/> |
| <dl> <dt>**SES \_ EX \_ USEMOUSEWPARAM**</dt> </dl>     | Verwenden *Sie wParam,* wenn Sie die [**WM \_ MOUSEMOVE-Nachricht**](/windows/desktop/inputdev/wm-mousemove) behandeln, und rufen Sie [**getAsyncKeyState nicht auf.**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)<br/>                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md)
</dt> </dl>

 

