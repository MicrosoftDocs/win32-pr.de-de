---
title: EM_GETELLIPSISMODE Meldung (RichEdit. h)
description: Ruft den aktuellen Ellipsen Modus ab.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- Windows-Steuerelemente für EM_GETELLIPSISMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103785"
---
# <a name="em_getellipsismode-message"></a>EM \_ getellipsismode-Meldung

Ruft den aktuellen Ellipsen Modus ab. Wenn diese Option aktiviert ist, wird ein Auslassungs Zeichen () für Text angezeigt, der nicht in das Anzeige Fenster passt. Die Ellipse wird nur verwendet, wenn das Steuerelement nicht aktiv ist. Wenn aktiv, werden Scrollleisten verwendet, um Text anzuzeigen, der nicht in das Anzeige Fenster passt.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein DWORD-Wert, der einen der folgenden Werte empfängt.



| Wert                                                                                                                                                         | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**Ellipse \_ None**</dt> </dl> | Es werden keine Ellipse verwendet.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**Ende der Auslassungs \_ Punkte**</dt> </dl>    | Ellipse am Ende (erzwungene Unterbrechung).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**Ellipse- \_ Wort**</dt> </dl> | Ellipse am Ende (Wort Umbruch).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn wParam gleich 0 und lParam nicht NULL ist, ist der Rückgabewert true. Andernfalls ist der Rückgabewert false.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM/ \_ tellipsismode**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ getellipsisstate**](em-getellipsisstate.md)
</dt> </dl>

 

 





