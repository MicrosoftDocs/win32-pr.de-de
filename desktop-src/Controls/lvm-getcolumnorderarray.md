---
title: LVM_GETCOLUMNORDERARRAY Meldung (kommstrg. h)
description: Ruft die aktuelle Reihenfolge von links nach rechts von Spalten in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getcolumnorderarray-Makro verwenden.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Windows-Steuerelemente für LVM_GETCOLUMNORDERARRAY Meldung
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
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040107"
---
# <a name="lvm_getcolumnorderarray-message"></a>LVM \_ getcolumnorderarray-Meldung

Ruft die aktuelle Reihenfolge von links nach rechts von Spalten in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**ListView \_ getcolumnorderarray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Spalten im Listenansicht-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von ganzen Zahlen, das die Indexwerte der Spalten im Listenansicht-Steuerelement empfängt. Das Array muss groß genug sein, um *wParam* -Elemente zu speichern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird ein Wert ungleich 0 (null) zurückgegeben, und der Puffer bei *LPARAM* empfängt den Spalten Index jeder Spalte im Steuerelement in der Reihenfolge, in der Sie von links nach rechts angezeigt werden. Andernfalls ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





