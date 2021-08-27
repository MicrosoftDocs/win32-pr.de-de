---
title: TDM_SET_MARQUEE_PROGRESS_BAR (Commctrl.h)
description: Gibt an, ob die gehostete Statusanzeige eines Aufgabendialogfelds im Festzeltmodus angezeigt werden soll.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13262339f7d87ea68755a38a49cc8c327706939d6b18025f350334dfdbe3dd4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104610"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>TDM \_ SET \_ MARQUEE \_ PROGRESS \_ BAR-Meldung

Gibt an, ob die gehostete Statusanzeige eines Aufgabendialogfelds im Festzeltmodus angezeigt werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Eine **BOOL,** die angibt, ob die Statusleiste im Festzeltmodus angezeigt werden soll. Der Wert **TRUE** aktiviert den Festzeltmodus, und der Wert **FALSE** deaktiviert den Festzeltmodus.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Informationen zum Festzeltmodus finden Sie unter [Statusleisten-Steuerelement](progress-bar-control.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





