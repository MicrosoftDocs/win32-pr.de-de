---
description: Eine Anwendung sendet die WM- \_ mdiiconarrange-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle minimierten untergeordneten MDI-Fenster anzuordnen. Untergeordnete Fenster, die nicht minimiert sind, sind nicht betroffen.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: WM_MDIICONARRANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484755"
---
# <a name="wm_mdiiconarrange-message"></a>WM- \_ mdiiconanordnen-Meldung

Eine Anwendung sendet die **WM- \_ mdiiconarrange** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle minimierten untergeordneten MDI-Fenster anzuordnen. Untergeordnete Fenster, die nicht minimiert sind, sind nicht betroffen.


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM- \_ mdicascade**](wm-mdicascade.md)
</dt> <dt>

[**WM- \_ mditile**](wm-mditile.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




