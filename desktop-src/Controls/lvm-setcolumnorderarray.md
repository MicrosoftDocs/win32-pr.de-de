---
title: LVM_SETCOLUMNORDERARRAY Nachricht (Commctrl.h)
description: Legt die Reihenfolge von links nach rechts von Spalten in einem Listenansichtssteuerelement fest. Sie können diese Nachricht explizit senden oder das ListView \_ SetColumnOrderArray-Makro verwenden.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 9931a7d2c12da02f928c21727292d7d1ce4a430790660afb99ede4bf717c38c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077300"
---
# <a name="lvm_setcolumnorderarray-message"></a>LVM \_ SETCOLUMNORDERARRAY-Nachricht

Legt die Reihenfolge von links nach rechts von Spalten in einem Listenansichtssteuerelement fest. Sie können diese Nachricht explizit senden oder das [**ListView \_ SetColumnOrderArray-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Größe des Puffers in Elementen bei *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array, das die Reihenfolge angibt, in der Spalten von links nach rechts angezeigt werden sollen. Wenn der Inhalt des Arrays beispielsweise ist, {2,0,1} zeigt das Steuerelement die Spalten 2, 0 und 1 in dieser Reihenfolge an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





