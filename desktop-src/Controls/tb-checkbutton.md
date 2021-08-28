---
title: TB_CHECKBUTTON (Commctrl.h)
description: Überprüft oder deaktiviert eine bestimmte Schaltfläche in einer Symbolleiste.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- TB_CHECKBUTTON meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec35b6a333e0663acc8c94dec22c2b8f4138cb6024b1f7919fd0ec73cdb0eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919130"
---
# <a name="tb_checkbutton-message"></a>TB \_ CHECKBUTTON-Meldung

Überprüft oder deaktiviert eine bestimmte Schaltfläche in einer Symbolleiste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Befehlsbezeichner der zu überprüfenden Schaltfläche.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**ist**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) eine **BOOL,** die angibt, ob die angegebene Schaltfläche überprüft oder deaktiviert werden soll. True **gibt an,** dass die Überprüfung hinzugefügt wird. False **gibt an,** dass die Überprüfung entfernt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Wenn eine Schaltfläche überprüft wird, wird sie im gedrückten Zustand angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

