---
title: RB_SETCOLORSCHEME Meldung (kommstrg. h)
description: Legt die Farbschema Informationen für das Grund leisten-Steuerelement fest.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- Windows-Steuerelemente für RB_SETCOLORSCHEME Meldung
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517963"
---
# <a name="rb_setcolorscheme-message"></a>RB \_ SetColorScheme-Meldung

Legt die Farbschema Informationen für das Grund leisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) -Struktur, die die Farbschema Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Das Grund leisten-Steuerelement verwendet die Farbschema Informationen beim Zeichnen der 3D-Elemente im Steuerelement und den Bändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ getcolorscheme**](rb-getcolorscheme.md)
</dt> </dl>

 

 





