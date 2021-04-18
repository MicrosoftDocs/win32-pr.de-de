---
title: MCIWNDM_CHANGESTYLES Meldung (VFW. h)
description: Die mciwndm \_ changestyles-Meldung ändert die vom mciwnd-Fenster verwendeten Stile. Sie können diese Nachricht explizit oder mithilfe des mciwndchangestyles-Makros senden.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340313"
---
# <a name="mciwndm_changestyles-message"></a>Mciwndm \_ changestyles-Nachricht

Die **mciwndm \_ changestyles** -Meldung ändert die vom mciwnd-Fenster verwendeten Stile. Sie können diese Nachricht explizit oder mithilfe des [**mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) -Makros senden.


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*chel*
</dt> <dd>

Maske, die die Stile identifiziert, die geändert werden können. Diese Maske ist der bitweise OR-Operator aller Stile, die geändert werden dürfen.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Neue Stileinstellungen für das Fenster. Geben Sie 0 (null) für diesen Parameter an, um alle in der Maske identifizierten Stile zu deaktivieren. Eine Liste der verfügbaren Stile finden Sie unter der Funktion " [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**Mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





