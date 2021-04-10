---
title: RB_GETBARINFO Meldung (kommstrg. h)
description: Ruft Informationen zum Grund leisten-Steuerelement und der von ihm verwendeten Bildliste ab.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- Windows-Steuerelemente für RB_GETBARINFO Meldung
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040793"
---
# <a name="rb_getbarinfo-message"></a>RB \_ getbarinfo-Meldung

Ruft Informationen zum Grund leisten-Steuerelement und der von ihm verwendeten Bildliste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**rebarinfo**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) -Struktur, die die Informationen zum Info leisten-Steuerelement empfängt. Sie müssen den **CBSIZE** -Member dieser Struktur auf **sizeof**(rebarinfo) festlegen, bevor Sie diese Nachricht senden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





