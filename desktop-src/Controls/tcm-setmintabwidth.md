---
title: TCM_SETMINTABWIDTH Meldung (kommstrg. h)
description: Legt die minimale Breite von Elementen in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ setmintabwidth-Makros senden.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- Windows-Steuerelemente für TCM_SETMINTABWIDTH Meldung
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340758"
---
# <a name="tcm_setmintabwidth-message"></a>TCM- \_ setmintabwidth-Meldung

Legt die minimale Breite von Elementen in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ setmintabwidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Minimale Breite, die für ein Registerkarten-Steuerelement festgelegt werden soll. Wenn dieser Parameter auf-1 festgelegt ist, verwendet das Steuerelement die Standard Registerkarten Breite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die vorherige minimale Registerkarten Breite darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





