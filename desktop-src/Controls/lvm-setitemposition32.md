---
title: LVM_SETITEMPOSITION32 Meldung (kommstrg. h)
description: Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Windows-Steuerelemente für LVM_SETITEMPOSITION32 Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040666"
---
# <a name="lvm_setitemposition32-message"></a>LVM \_ SETITEMPOSITION32 Meldung

Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden). Diese Meldung unterscheidet sich von der Nachricht [**LVM \_**](lvm-setitemposition.md) -Nachricht, dass Sie 32-Bit-Koordinaten verwendet. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements, für das die Position festgelegt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die neue Position des Elements in Listen Ansichts Koordinaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

