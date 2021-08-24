---
title: LVM_SETITEMPOSITION32 Meldung (Commctrl.h)
description: Verschiebt ein Element an eine angegebene Position in einem Listenansichtssteuerelement (muss sich in der Symbolansicht oder kleinen Symbolansicht befinden).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 737b9aa78067bd4851c907da4ac51bd2645a833d8f3335c90a6e81a902d3a30a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656250"
---
# <a name="lvm_setitemposition32-message"></a>LVM \_ SETITEMPOSITION32-Nachricht

Verschiebt ein Element an eine angegebene Position in einem Listenansichtssteuerelement (muss sich in der Symbolansicht oder kleinen Symbolansicht befinden). Diese Nachricht unterscheidet sich von der [**LVM \_ SETITEMPOSITION-Nachricht**](lvm-setitemposition.md) darin, dass sie 32-Bit-Koordinaten verwendet. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Listenansichtselements, für das die Position festgelegt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf [](/previous-versions//dd162805(v=vs.85)) eine POINT-Struktur, die die neue Position des Elements in Listenansichtskoordinaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

