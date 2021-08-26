---
title: LVM_DELETECOLUMN Nachricht (Commctrl.h)
description: Entfernt eine Spalte aus einem Listenansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ DeleteColumn-Makros senden.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039ab92028d23a75518237bc6e9723f051f2f6f2de8732e40f2086d027a61873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920320"
---
# <a name="lvm_deletecolumn-message"></a>LVM \_ DELETECOLUMN-Nachricht

Entfernt eine Spalte aus einem Listenansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ DeleteColumn-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der zu löschenden Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Das Löschen der Spalte 0 (null) eines Listenansichtssteuerelements wird nur in ComCtl32.dll Version 6 und höher unterstützt. Version 5 unterstützt auch das Löschen der Spalte 0 (null), jedoch erst, nachdem Sie [**CCM \_ SETVERSION**](ccm-setversion.md) verwendet haben, um die Version auf 5 oder höher festzulegen. Wenn Sie in Versionen vor Version 5 die Spalte 0 (null) löschen müssen, fügen Sie eine Dummyspalte 0 (null) ein, und löschen Sie die Spalte 1 und höher.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





