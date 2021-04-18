---
title: TB_SETBUTTONSIZE Meldung (kommstrg. h)
description: Legt die Größe der Schaltflächen auf einer Symbolleiste fest.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Windows-Steuerelemente für TB_SETBUTTONSIZE Meldung
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345295"
---
# <a name="tb_setbuttonsize-message"></a>TB \_ setbuttonsize-Meldung

Legt die Größe der Schaltflächen auf einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Breite der Schaltflächen in Pixel an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Höhe der Schaltflächen in Pixel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

**TB \_ Setbuttonsize** sollte in der Regel nach dem Hinzufügen von Schaltflächen aufgerufen werden.

Legen Sie mit " [**TB \_ setbuttonwidth**](tb-setbuttonwidth.md) " die maximale und minimale zulässige Breite für Schaltflächen fest, bevor Sie hinzugefügt werden. Legen Sie die tatsächliche Größe von Schaltflächen mit **TB \_ setbuttonsize** fest.

## <a name="examples"></a>Beispiele

Im folgenden Beispielcode wird die Breite von Schaltflächen auf 80 Pixel und die Höhe auf 30 Pixel festgelegt.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

