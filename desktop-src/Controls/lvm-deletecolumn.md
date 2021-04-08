---
title: LVM_DELETECOLUMN Meldung (kommstrg. h)
description: Entfernt eine Spalte aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ deleteColumn-Makros senden.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- Windows-Steuerelemente für LVM_DELETECOLUMN Meldung
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
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739969"
---
# <a name="lvm_deletecolumn-message"></a>LVM \_ deleteColumn-Nachricht

Entfernt eine Spalte aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ deleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der zu löschenden Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das Löschen der Spalte NULL eines Listenansicht-Steuer Elements wird nur in ComCtl32.dll Version 6 und höher unterstützt. Version 5 unterstützt auch das Löschen von Spalten NULL, aber erst nach der Verwendung von [**ccm \_ setVersion**](ccm-setversion.md) , um die Version auf 5 oder höher festzulegen. Wenn Sie in Versionen vor Version 5 die Spalte NULL löschen müssen, fügen Sie eine dummyspalte der Länge 0 (null) ein, und löschen Sie die Spalte 1 und höher.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





