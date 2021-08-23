---
title: MCIWNDM_CHANGESTYLES (Vfw.h)
description: Die MCIWNDM \_ CHANGESTYLES-Meldung ändert die vom MCIWnd-Fenster verwendeten Stile. Sie können diese Nachricht explizit oder mithilfe des MCIWndChangeStyles-Makros senden.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES-Nachricht Windows Multimedia
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
ms.openlocfilehash: 5525066f4c377cc093e1e7a0dedd4edf7463792c136214a519da9744917cbc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525510"
---
# <a name="mciwndm_changestyles-message"></a>MCIWNDM \_ CHANGESTYLES-Nachricht

Die **MCIWNDM \_ CHANGESTYLES-Meldung** ändert die vom MCIWnd-Fenster verwendeten Stile. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndChangeStyles-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) senden.


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*Maske*
</dt> <dd>

Maske, die die Stile identifiziert, die sich ändern können. Diese Maske ist der bitweise OR-Operator aller Stile, die geändert werden dürfen.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Neue Stileinstellungen für das Fenster. Geben Sie 0 (null) für diesen Parameter an, um alle in der Maske identifizierten Stile zu deaktivieren. Eine Liste der verfügbaren Stile finden Sie in der [**MCIWndCreate-Funktion.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





