---
title: LVM_SETCOLUMNORDERARRAY Meldung (kommstrg. h)
description: Legt die Reihenfolge der Spalten in einem Listenansicht-Steuerelement von links nach rechts fest. Sie können diese Nachricht explizit senden oder das ListView \_ setcolumnorderarray-Makro verwenden.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Windows-Steuerelemente für LVM_SETCOLUMNORDERARRAY Meldung
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040099"
---
# <a name="lvm_setcolumnorderarray-message"></a>LVM- \_ setcolumnorderarray-Meldung

Legt die Reihenfolge der Spalten in einem Listenansicht-Steuerelement von links nach rechts fest. Sie können diese Nachricht explizit senden oder das [**ListView \_ setcolumnorderarray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Größe des Puffers in *LPARAM* in-Elementen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array, das die Reihenfolge angibt, in der Spalten von links nach rechts angezeigt werden sollen. Wenn der Inhalt des Arrays beispielsweise {2,0,1} ist, zeigt das Steuerelement Spalte 2, Spalte 0 und Spalte 1 in dieser Reihenfolge an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





