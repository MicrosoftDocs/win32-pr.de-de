---
title: LVM_HITTEST Meldung (kommstrg. h)
description: Bestimmt, welches Listen Ansichts Element, sofern vorhanden, an einer angegebenen Position liegt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ HitTest-Makros senden.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Windows-Steuerelemente für LVM_HITTEST Meldung
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956983"
---
# <a name="lvm_hittest-message"></a>LVM- \_ HitTest-Meldung

Bestimmt, welches Listen Ansichts Element, sofern vorhanden, an einer angegebenen Position liegt. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss den Wert 0 (null) haben. **Windows Vista.** Sollte-1 sein, wenn die Elemente **igroup** und **iSubItem** der *LPARAM* -Struktur abgerufen werden sollen.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine " [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) "-Struktur, die die Position zum Treffer Test enthält und Informationen zu den Ergebnissen des Treffer Tests empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements an der angegebenen Position zurück, falls vorhanden, andernfalls-1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





