---
title: LVM_GETBKIMAGE Meldung (kommstrg. h)
description: Ruft das Hintergrundbild in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getbkimage-Makros senden.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- Windows-Steuerelemente für LVM_GETBKIMAGE Meldung
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739960"
---
# <a name="lvm_getbkimage-message"></a>LVM \_ getbkimage-Nachricht

Ruft das Hintergrundbild in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getbkimage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine " [**lvbkimage**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) "-Struktur, die die Hintergrundbild Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Getbkimagew** (Unicode) und **LVM \_ getbkimagea** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM- \_ setbkimage**](lvm-setbkimage.md)
</dt> </dl>

 

 





