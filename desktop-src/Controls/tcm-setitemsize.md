---
title: TCM_SETITEMSIZE Meldung (Commctrl.h)
description: Legt die Breite und Höhe von Registerkarten in einem Steuerelement mit fester Breite oder einem besitzergezeichneten Registerkartensteuerelement fest. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl-Makros SetItemSize senden.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 8845aa54cd3cca413f31ee01f4a9583e24dc875a876d1aff691f574214f6f793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876230"
---
# <a name="tcm_setitemsize-message"></a>TCM \_ SETITEMSIZE-Nachricht

Legt die Breite und Höhe von Registerkarten in einem Steuerelement mit fester Breite oder einem besitzergezeichneten Registerkartensteuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ TabCtrl-Makros SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **INT-Wert,** der die neue Breite in Pixel angibt. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **INT-Wert,** der die neue Höhe in Pixel angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die alte Breite und Höhe zurück. Die Breite befindet sich im [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des Rückgabewerts, und die Höhe befindet sich im [**HIWORD.**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))

## <a name="remarks"></a>Hinweise

Wenn die Breite auf einen Wert kleiner als die von [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)festgelegte Bildbreite festgelegt ist, wird die Breite der Registerkarte auf den niedrigsten Wert festgelegt, der größer als die Bildbreite ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

