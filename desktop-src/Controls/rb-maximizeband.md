---
title: RB_MAXIMIZEBAND Meldung (kommstrg. h)
description: Ändert die Größe eines Bands in einem Grund leisten-Steuerelement entweder auf seine ideale oder größte Größe.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- Windows-Steuerelemente für RB_MAXIMIZEBAND Meldung
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859070"
---
# <a name="rb_maximizeband-message"></a>RB \_ maximizeband-Meldung

Ändert die Größe eines Bands in einem Grund leisten-Steuerelement entweder auf seine ideale oder größte Größe.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des zu maximier enden Bands.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, ob die ideale Breite des Bands verwendet werden soll, wenn das Band maximiert ist. Wenn dieser Wert ungleich 0 (null) ist, wird die ideale Breite verwendet. Wenn dieser Wert 0 (null) ist, wird das Band so groß wie möglich gemacht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**RB \_ SetBandInfo**](rb-setbandinfo.md)
</dt> </dl>

 

 





