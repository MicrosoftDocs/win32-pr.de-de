---
title: TCM_SETPADDING Meldung (kommstrg. h)
description: Legt den Leerraum (Padding) um das Symbol und die Bezeichnung der einzelnen Registerkarten in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg- \_ setPadding-Makros senden.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- Windows-Steuerelemente für TCM_SETPADDING Meldung
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
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338318"
---
# <a name="tcm_setpadding-message"></a>TCM- \_ setPadding-Meldung

Legt den Leerraum (Padding) um das Symbol und die Bezeichnung der einzelnen Registerkarten in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg- \_ setPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **int** -Wert, der die horizontale Auffüll Menge in Pixel angibt. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **int** -Wert, der die Menge der vertikalen Auffüll Zeichen in Pixel angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

