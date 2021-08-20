---
title: RB_GETCOLORSCHEME Meldung (Commctrl.h)
description: Ruft die Farbschemainformationen aus dem Steuerelement für die Neuleiste ab.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- RB_GETCOLORSCHEME Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918b46d1077c0074584be2d609d486097cc2e40f7a5c62a03db914fce58e320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169620"
---
# <a name="rb_getcolorscheme-message"></a>RB \_ GETCOLORSCHEME-Nachricht

Ruft die Farbschemainformationen aus dem Steuerelement für die Neuleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**COLORSCHEME-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) die die Farbschemainformationen empfängt. Sie müssen den **dwSize-Member** dieser Struktur auf **sizeof**(COLORSCHEME) festlegen, bevor Sie diese Nachricht senden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)
</dt> </dl>

 

 





