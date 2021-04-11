---
title: RB_GETRECT Meldung (kommstrg. h)
description: Ruft das umschließende Rechteck für ein bestimmtes Band in einem Grund leisten-Steuerelement ab.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- Windows-Steuerelemente für RB_GETRECT Meldung
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213721"
---
# <a name="rb_getrect-message"></a>RB \_ GetRect-Nachricht

Ruft das umschließende Rechteck für ein bestimmtes Band in einem Grund leisten-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index eines Bands im Grund leisten-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Begrenzungen des Bereichs der Info Leiste empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

