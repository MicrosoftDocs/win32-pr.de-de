---
title: EM_DISPLAYBAND Nachricht (Richedit.h)
description: Zeigt einen Teil des Inhalts eines Rich Edit-Steuerelements an, wie zuvor für ein Gerät mithilfe der EM \_ FORMATRANGE-Nachricht formatiert.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67fc951940d76dced2851a01b7049b053f3e3c2b45f6eee95eb27bef633f59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915940"
---
# <a name="em_displayband-message"></a>EM \_ DISPLAYBAND-Meldung

Zeigt einen Teil des Inhalts eines Rich Edit-Steuerelements an, wie zuvor für ein Gerät mithilfe der [**EM \_ FORMATRANGE-Nachricht**](em-formatrange.md) formatiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die den Anzeigebereich des Geräts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn der Vorgang fehlschlägt, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Text- und Component Object Model-Objekte (COM) werden vom Rechteck abgeschnitten. Die Anwendung muss den Ausschneidebereich nicht festlegen.

Banding ist der Prozess, mit dem eine einzelne Ausgabeseite mit einem oder mehreren separaten Rechtecke oder Bändern generiert wird. Wenn alle Bänder auf der Seite platziert werden, wird ein vollständiges Bild angezeigt. Dieser Ansatz wird häufig von Rasterdruckern verwendet, die nicht über genügend Arbeitsspeicher verfügen oder eine vollständige Seite gleichzeitig abbilden können. Bandgeräte umfassen die meisten Dot Matrix-Drucker sowie einige Drucker für Drucker.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken von Rich Edit-Steuerelementen](printing-rich-edit-controls.md)
</dt> </dl>

 

