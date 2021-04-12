---
title: SB_SIMPLE Meldung (kommstrg. h)
description: Gibt an, ob ein Statusfenster einfachen Text anzeigt oder alle durch eine vorherige SB SetParts-Meldung festgelegten Fensterteile anzeigt \_ .
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- Windows-Steuerelemente für SB_SIMPLE Meldung
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105063"
---
# <a name="sb_simple-message"></a>Einfache SB- \_ Nachricht

Gibt an, ob ein Statusfenster einfachen Text anzeigt oder alle durch eine vorherige [**SB \_ SetParts**](sb-setparts.md) -Meldung festgelegten Fensterteile anzeigt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag des Anzeige Typs. Wenn dieser Parameter **true** ist, wird im Fenster einfacher Text angezeigt. Wenn der Wert **false** ist, werden mehrere Teile angezeigt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Wenn das Statusfenster von nicht einfache in Simple geändert wird oder umgekehrt, wird das Fenster sofort neu gezeichnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





