---
title: MCIWNDM_SETZOOM (Vfw.h)
description: Mit der MCIWNDM SETZOOM-Nachricht wird die Größe eines \_ Videobilds entsprechend einem Zoomfaktor geändert. Dieses Fenster passt die Größe eines MCIWnd-Fensters an, während gleichzeitig ein konstantes Seitenverhältnis beibehalten wird. Sie können diese Nachricht explizit oder mithilfe des MCIWndSetZoom-Makros senden.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM von Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcdd40206332df442bbae32975b0d888bbe39bc377a189d40e215888e4a6d0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807580"
---
# <a name="mciwndm_setzoom-message"></a>MCIWNDM \_ SETZOOM-Meldung

Mit **der MCIWNDM \_ SETZOOM-Nachricht** wird die Größe eines Videobilds entsprechend einem Zoomfaktor geändert. Dieses Fenster passt die Größe eines MCIWnd-Fensters an, während gleichzeitig ein konstantes Seitenverhältnis beibehalten wird. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndSetZoom-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) senden.


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*
</dt> <dd>

Zoomfaktor, ausgedrückt als Prozentsatz des ursprünglichen Bilds. Geben Sie 100 an, um das Bild in seiner erstellungsgröße anzuzeigen, 200, um das Bild mit doppelter Normalgröße anzuzeigen, oder 50, um das Bild in der Hälfte seiner normalen Größe anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





