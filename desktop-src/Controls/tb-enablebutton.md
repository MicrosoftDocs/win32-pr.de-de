---
title: TB_ENABLEBUTTON Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert die angegebene Schaltfläche in einer Symbolleiste.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- Windows-Steuerelemente für TB_ENABLEBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342885"
---
# <a name="tb_enablebutton-message"></a>TB \_ enablebutton-Meldung

Aktiviert oder deaktiviert die angegebene Schaltfläche in einer Symbolleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Befehls Bezeichner der Schaltfläche, die aktiviert oder deaktiviert werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob die angegebene Schaltfläche aktiviert oder deaktiviert werden soll. **True** gibt an, dass die Schaltfläche aktiviert ist. Wenn der Wert **false** ist, wird die Schaltfläche deaktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn eine Schaltfläche aktiviert wurde, kann Sie gedrückt und aktiviert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

