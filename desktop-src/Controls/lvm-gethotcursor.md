---
title: LVM_GETHOTCURSOR Nachricht (Commctrl.h)
description: Ruft den HCURSOR-Wert ab, der verwendet wird, wenn sich der Zeiger über einem Element befindet, während die Heiße Nachverfolgung aktiviert ist. Sie können diese Nachricht explizit senden oder das ListView \_ GetHotCursor-Makro verwenden.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5703d252d239124b78656c4a5991efdecb2107552fb6e2ab0f87701af4e18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540800"
---
# <a name="lvm_gethotcursor-message"></a>LVM \_ GETHOTCURSOR-Nachricht

Ruft den HCURSOR-Wert ab, der verwendet wird, wenn sich der Zeiger über einem Element befindet, während die Heiße Nachverfolgung aktiviert ist. Sie können diese Nachricht explizit senden oder das [**ListView \_ GetHotCursor-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen HCURSOR-Wert zurück, der das Handle für den Cursor darstellt, den das Listenansichtssteuerelement verwendet, wenn hot tracking aktiviert ist.

## <a name="remarks"></a>Hinweise

Ein Listenansichtssteuerelement verwendet die heiße Nachverfolgung und die Auswahl mit dem Mauszeiger, wenn der [**LVS \_ EX \_ TRACKSELECT-Stil**](extended-list-view-styles.md) festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





