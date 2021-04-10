---
title: EM_GETCHARFORMAT Meldung (RichEdit. h)
description: Bestimmt die Zeichen Formatierung in einem Rich-Edit-Steuerelement.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Windows-Steuerelemente für EM_GETCHARFORMAT Meldung
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040692"
---
# <a name="em_getcharformat-message"></a>EM \_ getcharformat-Meldung

Bestimmt die Zeichen Formatierung in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Textbereich an, aus dem die Formatierung abgerufen wird. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                         | Bedeutung                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF- \_ Standard**</dt> </dl>       | Die Standard Zeichen Formatierung.<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**SCF- \_ Auswahl**</dt> </dl> | Die Zeichen Formatierung der aktuellen Auswahl.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur, die die Attribute des ersten Zeichens empfängt. Der **dwMask** -Member gibt an, welche Attribute in der gesamten Auswahl konsistent sind. Wenn die gesamte Auswahl z. b. entweder kursiv oder nicht kursiv formatiert ist, wird cfm \_ Italic festgelegt. wenn die Auswahl teilweise kursiv und teilweise nicht ist, wird cfm \_ Italic nicht festgelegt.

Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) -Struktur sein, die eine Erweiterung der [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur ist. Vor dem Senden der **EM \_ getcharformat** -Meldung legen Sie den **CBSIZE** -Member der Struktur so fest, dass die Version der Struktur angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den Wert des **dwMask** -Members der [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





