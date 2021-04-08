---
title: LVM_ENSUREVISIBLE Meldung (kommstrg. h)
description: Stellt sicher, dass ein Listen Ansichts Element entweder vollständig oder teilweise sichtbar ist, und führt ggf. einen Bildlauf im Listenansicht-Steuerelement durch Sie können diese Nachricht explizit oder mithilfe des ListView \_ EnsureVisible-Makros senden.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- Windows-Steuerelemente für LVM_ENSUREVISIBLE Meldung
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949427"
---
# <a name="lvm_ensurevisible-message"></a>LVM \_ EnsureVisible-Meldung

Stellt sicher, dass ein Listen Ansichts Element entweder vollständig oder teilweise sichtbar ist, und führt ggf. einen Bildlauf im Listenansicht-Steuerelement durch Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein-Wert, der angibt, ob das Element vollständig sichtbar sein muss. Wenn dieser Parameter **true** ist, wird kein Bildlauf durchgeführt, wenn das Element mindestens teilweise sichtbar ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Meldung schlägt fehl, wenn der Fenster Stil [**LVS \_ NoScroll**](list-view-window-styles.md)enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





