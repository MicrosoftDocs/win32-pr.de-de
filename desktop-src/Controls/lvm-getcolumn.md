---
title: LVM_GETCOLUMN Meldung (kommstrg. h)
description: Ruft die Attribute der Spalte eines Listenansicht-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetColumn-Makros senden.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Windows-Steuerelemente für LVM_GETCOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475174"
---
# <a name="lvm_getcolumn-message"></a>LVM \_ GetColumn-Nachricht

Ruft die Attribute der Spalte eines Listenansicht-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der Spalte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur, die die Informationen angibt, die abgerufen werden sollen, und die Informationen über die Spalte empfängt. Der **Mask** -Member gibt an, welche Spalten Attribute abgerufen werden sollen. Wenn das **Mask** -Element den "lvcf" \_ -Textwert angibt, muss der **pszText** -Member die Adresse des Puffers enthalten, der den Element Text empfängt, und der **cchtextmax** -Member muss die Größe des Puffers angeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





