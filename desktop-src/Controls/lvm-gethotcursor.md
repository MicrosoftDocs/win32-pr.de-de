---
title: LVM_GETHOTCURSOR Meldung (kommstrg. h)
description: Ruft den hcursor-Wert ab, der verwendet wird, wenn sich der Zeiger über einem Element befindet, während Hot Tracking aktiviert ist. Sie können diese Nachricht explizit senden oder das ListView \_ gethotcursor-Makro verwenden.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- Windows-Steuerelemente für LVM_GETHOTCURSOR Meldung
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
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743008"
---
# <a name="lvm_gethotcursor-message"></a>LVM- \_ gethotcursor-Nachricht

Ruft den hcursor-Wert ab, der verwendet wird, wenn sich der Zeiger über einem Element befindet, während Hot Tracking aktiviert ist. Sie können diese Nachricht explizit senden oder das [**ListView \_ gethotcursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen hcursor-Wert zurück, der das Handle für den Cursor ist, den das Listenansicht-Steuerelement verwendet, wenn die Hot-Nachverfolgung aktiviert ist.

## <a name="remarks"></a>Bemerkungen

Ein Listenansicht-Steuerelement verwendet die Hot-Tracking-und Hover-Auswahl, wenn der [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md) -Stil festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





