---
title: HDM_SETITEM Nachricht (Commctrl.h)
description: Legt die Attribute des angegebenen Elements in einem Headersteuerelement fest. Sie können diese Nachricht explizit senden oder das \_ HeadersetItem-Makro verwenden.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd0e2709a1b40bd4a564498cd0ae0b5d4e11861066aa9b0951815f92ee1c295f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171065"
---
# <a name="hdm_setitem-message"></a>HDM \_ SETITEM-Nachricht

Legt die Attribute des angegebenen Elements in einem Headersteuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ HeadersetItem-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der aktuelle Index des Elements, dessen Attribute geändert werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-hditema) die Elementinformationen enthält. Wenn diese Nachricht gesendet wird, muss der **Maskenmember** der -Struktur festgelegt werden, um anzugeben, welche Attribute festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

Die [**HDITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-hditema) die diese Nachricht unterstützt, unterstützt Elementreihenfolge- und Bildlisteninformationen. Mit diesen Membern können Sie die Reihenfolge steuern, in der Elemente angezeigt werden, und Bilder angeben, die mit Elementen angezeigt werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDM \_ SETITEMW** (Unicode) und **HDM \_ SETITEMA** (ANSI)<br/>                   |



 

 





