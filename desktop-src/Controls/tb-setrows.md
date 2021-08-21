---
title: TB_SETROWS (Commctrl.h)
description: Legt die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste fest.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2c0e95d6f0f19c2b1c9b76cf22a37da0086987b22fe144603cdb2afa8a1ad83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293640"
---
# <a name="tb_setrows-message"></a>TB \_ SETROWS-Nachricht

Legt die Anzahl der Zeilen von Schaltflächen in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die Anzahl der angeforderten Zeilen an. Die Mindestanzahl von Zeilen ist 1, und die maximale Anzahl von Zeilen entspricht der Anzahl der Schaltflächen in der Symbolleiste.

Das [**HIWORD ist**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) eine **BOOL,** die angibt, ob mehr Zeilen als angefordert erstellt werden sollen, wenn das System die von *wParam* angegebene Anzahl von Zeilen nicht erstellen kann. True **gibt an,** dass das System weitere Zeilen erstellt. False **gibt an,** dass das System weniger Zeilen erstellt.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die das umgebundene Rechteck der Symbolleiste empfängt, nachdem die Zeilen festgelegt wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Da das System beim Festlegen der Anzahl von Zeilen keine Schaltflächengruppen aufbricht, kann sich die resultierende Anzahl von Zeilen von der angeforderten Anzahl unterscheiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

