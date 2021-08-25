---
title: TDM_SET_PROGRESS_BAR_RANGE Nachricht (Commctrl.h)
description: Legt die Minimal- und Höchstwerte für die Statusanzeige in einem Aufgabendialogfeld fest.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d94da64bd01b17addeb8f65def177e7e7e5d7daccbafb1629d1158f8c6636d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875910"
---
# <a name="tdm_set_progress_bar_range-message"></a>TDM \_ SET PROGRESS BAR RANGE \_ \_ \_ message

Legt die Minimal- und Höchstwerte für die Statusanzeige in einem Aufgabendialogfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Minimalwert an. Standardmäßig ist der Mindestwert 0 (null). [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Maximalwert an. Standardmäßig ist der Höchstwert 100.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherigen Mindest- und Höchstwerte zurück, falls erfolgreich, oder 0 (null). [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Minimalwert, und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält den Höchstwert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

