---
title: LVM_GETEXTENDEDLISTVIEWSTYLE Meldung (kommstrg. h)
description: Ruft die erweiterten Stile ab, die zurzeit für ein angegebenes Listenansicht-Steuerelement verwendet werden. Sie können diese Nachricht explizit senden oder das ListView \_ getextendedlistviewstyle-Makro verwenden.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Windows-Steuerelemente für LVM_GETEXTENDEDLISTVIEWSTYLE Meldung
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
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040103"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>LVM \_ getextendedlistviewstyle-Meldung

Ruft die erweiterten Stile ab, die zurzeit für ein angegebenes Listenansicht-Steuerelement verwendet werden. Sie können diese Nachricht explizit senden oder das [**ListView \_ getextendedlistviewstyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD** zurück, das die derzeit für ein angegebenes Listenansicht-Steuerelement verwendeten Stile darstellt. Bei diesem Wert kann es sich um eine Kombination aus [erweiterten List-View Stilen](extended-list-view-styles.md)handeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





