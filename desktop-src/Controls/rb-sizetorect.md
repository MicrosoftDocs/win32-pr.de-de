---
title: RB_SIZETORECT (Commctrl.h)
description: Versucht, das beste Layout der Bänder für das gegebene Rechteck zu finden.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63630fc64f56dff914b4fb576ecc6cef43d12d192606a5088924fd6a5832e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078549"
---
# <a name="rb_sizetorect-message"></a>RB \_ SIZETORECT-Meldung

Versucht, das beste Layout der Bänder für das gegebene Rechteck zu finden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die das Rechteck angibt, auf das das Rebar-Steuerelement festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn eine Layoutänderung aufgetreten ist, andernfalls 0 (null).

## <a name="remarks"></a>Hinweise

Die Bänder der Leiste werden nach Bedarf so angeordnet und umschlossen, dass sie dem Rechteck passen. Bänder mit dem Stil RBBS VARIABLEHEIGHT werden so gleichmäßig wie möglich an das \_ Rechteck geändert. Die Höhe einer horizontalen Leiste oder die Breite einer vertikalen Leiste kann sich abhängig vom neuen Layout ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

