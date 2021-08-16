---
title: LVM_GETEXTENDEDLISTVIEWSTYLE (Commctrl.h)
description: Ruft die erweiterten Stile ab, die derzeit für ein bestimmtes Listenansicht-Steuerelement verwendet werden. Sie können diese Nachricht explizit senden oder das ListView \_ GetExtendedListViewStyle-Makro verwenden.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04b2f83f5a8bd55f01aa84e315512c5ccb1b28b17f196c0199fc417544a6737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968300"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>LVM \_ GETEXTENDEDLISTVIEWSTYLE-Nachricht

Ruft die erweiterten Stile ab, die derzeit für ein bestimmtes Listenansicht-Steuerelement verwendet werden. Sie können diese Nachricht explizit senden oder das [**ListView \_ GetExtendedListViewStyle-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD zurück,** das die Derzeit für ein bestimmtes Listenansicht-Steuerelement verwendeten Stile darstellt. Dieser Wert kann eine Kombination aus erweiterten List-View [Sein.](extended-list-view-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





