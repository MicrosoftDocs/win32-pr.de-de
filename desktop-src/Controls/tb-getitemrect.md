---
title: TB_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck einer Schaltfläche in einer Symbolleiste ab.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- Windows-Steuerelemente für TB_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859103"
---
# <a name="tb_getitemrect-message"></a>TB- \_ GetItemRect-Nachricht

Ruft das umgebende Rechteck einer Schaltfläche in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index der Schaltfläche, für die Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Client Koordinaten des umschließenden Rechtecks empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Nachricht ruft nicht das umgebende Rechteck für Schaltflächen ab, deren Zustand auf den [**ausgeblendeten \_ TBSTATE**](toolbar-button-states.md) -Wert festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

