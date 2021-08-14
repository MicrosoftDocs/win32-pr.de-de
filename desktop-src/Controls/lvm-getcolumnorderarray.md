---
title: LVM_GETCOLUMNORDERARRAY Meldung (Commctrl.h)
description: Ruft die aktuelle Reihenfolge von links nach rechts von Spalten in einem Listenansichtssteuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ GetColumnOrderArray-Makro verwenden.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea54c633c7ffc9bc580609678e8ba5f62e29429aaea6f866bb7d72b6ea326eb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411496"
---
# <a name="lvm_getcolumnorderarray-message"></a>LVM \_ GETCOLUMNORDERARRAY-Nachricht

Ruft die aktuelle Reihenfolge von links nach rechts von Spalten in einem Listenansichtssteuerelement ab. Sie können diese Nachricht explizit senden oder das [**ListView \_ GetColumnOrderArray-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Spalten im Listenansichtssteuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von ganzen Zahlen, das die Indexwerte der Spalten im Listenansichtssteuerelement empfängt. Das Array muss groß genug sein, um *wParam-Elemente* zu enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt einen Wert ungleich 0 (null) zurück, und der Puffer bei *lParam* empfängt den Spaltenindex jeder Spalte im Steuerelement in der Reihenfolge, in der sie von links nach rechts angezeigt werden. Andernfalls ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





