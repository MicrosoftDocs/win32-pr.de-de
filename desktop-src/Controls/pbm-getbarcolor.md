---
title: PBM_GETBARCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe der Statusanzeige ab.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- Windows-Steuerelemente für PBM_GETBARCOLOR Meldung
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104799"
---
# <a name="pbm_getbarcolor-message"></a>PBM \_ getbarcolor-Meldung

Ruft die Farbe der Statusanzeige ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Farbe der Statusanzeige zurück.

## <a name="remarks"></a>Bemerkungen

Dies ist die Farbe, die von der [**PBM- \_ setbarcolor**](pbm-setbarcolor.md) -Nachricht festgelegt wird. Der Standardwert ist CLR \_ Default, der in "kommctrl. h" definiert ist.

Diese Funktion wirkt sich nur auf den klassischen Modus aus, nicht auf einen visuellen Stil.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





