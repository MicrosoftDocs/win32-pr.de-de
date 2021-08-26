---
title: LVM_ENSUREVISIBLE (Commctrl.h)
description: Stellt sicher, dass ein Listenansichtselement entweder vollständig oder teilweise sichtbar ist, und führt bei Bedarf einen Bildlauf durch das Listenansichtssteuerelement durch. Sie können diese Nachricht explizit oder mithilfe des Makros ListView \_ EnsureVisible senden.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE meldungssteuerelemente Windows
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
ms.openlocfilehash: baeefaf90f0a4562fb187024b2c6f8676c68fb9d46377a4ced900bda6cfd3dfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920300"
---
# <a name="lvm_ensurevisible-message"></a>LVM \_ ENSUREVISIBLE-Nachricht

Stellt sicher, dass ein Listenansichtselement entweder vollständig oder teilweise sichtbar ist, und führt bei Bedarf einen Bildlauf durch das Listenansichtssteuerelement durch. Sie können diese Nachricht explizit oder mithilfe des [**Makros ListView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listenansichtselements.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein -Wert, der an gibt, ob das Element vollständig sichtbar sein muss. Wenn dieser Parameter **TRUE ist,** erfolgt kein Bildlauf, wenn das Element zumindest teilweise sichtbar ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die Meldung schlägt fehl, wenn der Fensterstil [**LVS \_ NOSCROLL enthält.**](list-view-window-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





