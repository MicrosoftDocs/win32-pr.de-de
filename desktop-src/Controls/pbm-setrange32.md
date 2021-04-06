---
title: PBM_SETRANGE32 Meldung (kommstrg. h)
description: Legt den minimalen und maximalen Wert für eine Statusanzeige auf 32-Bit-Werte fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- Windows-Steuerelemente für PBM_SETRANGE32 Meldung
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742529"
---
# <a name="pbm_setrange32-message"></a>PBM \_ SETRANGE32 Meldung

Legt den minimalen und maximalen Wert für eine Statusanzeige auf 32-Bit-Werte fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Minimaler Bereichs Wert. Standardmäßig ist der Minimalwert 0 (null).

</dd> <dt>

*lParam* 
</dt> <dd>

Maximaler Bereichs Wert. Dieser Wert muss größer als *wParam* sein. Standardmäßig ist der Höchstwert 100.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der das vorherige 16-Bit-tiefstlimit in seinem [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und das vorherige 16-Bit-höchst Limit in seinem [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))-Wert enthält. Wenn die vorherigen Bereiche 32-Bit-Werte waren, besteht der Rückgabewert aus den **LoWord**-Werten der beiden 32-Bit-Limits.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**PBM- \_ GetRange**](pbm-getrange.md) -Nachricht, um die gesamten hohen und niedrigen 32-Bit-Werte abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

