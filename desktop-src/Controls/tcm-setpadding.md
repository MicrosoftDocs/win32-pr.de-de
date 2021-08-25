---
title: TCM_SETPADDING (Commctrl.h)
description: Legt den Abstand (Abstand) um das Symbol und die Bezeichnung der einzelnen Registerkarten in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem TabCtrl \_ SetPadding-Makro senden.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969ae3c7c240c38a6643682321c14e5744f2d2c2eec188004d1c3b2e6f2b3835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876240"
---
# <a name="tcm_setpadding-message"></a>TCM \_ SETPADDING-Meldung

Legt den Abstand (Abstand) um das Symbol und die Bezeichnung der einzelnen Registerkarten in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem [**TabCtrl \_ SetPadding-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

LOWORD [**ist**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ein **INT-Wert,** der die Menge der horizontalen Auf padding in Pixel angibt. Das [**HIWORD ist**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ein **INT-Wert,** der die Menge der vertikalen Auf padding in Pixel angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

