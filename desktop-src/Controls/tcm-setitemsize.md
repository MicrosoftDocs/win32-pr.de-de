---
title: TCM_SETITEMSIZE Meldung (kommstrg. h)
description: Legt die Breite und Höhe von Registerkarten in einem Registerkarten-Steuerelement mit fester Breite oder einem vom Besitzer gezeichneten Steuerelement fest Sie können diese Nachricht explizit oder mithilfe des tabctrl-Objekts tabstrg * senden \_ .
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- Windows-Steuerelemente für TCM_SETITEMSIZE Meldung
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858632"
---
# <a name="tcm_setitemsize-message"></a>TCM- \_ Nachricht

Legt die Breite und Höhe von Registerkarten in einem Registerkarten-Steuerelement mit fester Breite oder einem vom Besitzer gezeichneten Steuerelement fest Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Objekts \_ tabstrg**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) * senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **int** -Wert, der die neue Breite in Pixel angibt. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **int** -Wert, der die neue Höhe in Pixel angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die alte Breite und Höhe zurück. Die Breite liegt im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des Rückgabewerts, und die Höhe liegt im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))-Wert.

## <a name="remarks"></a>Bemerkungen

Wenn die Breite auf einen Wert festgelegt ist, der kleiner als die von [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)festgelegte Bildbreite ist, wird die Breite der Registerkarte auf den niedrigsten Wert festgelegt, der größer ist als die Breite des Bilds.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

