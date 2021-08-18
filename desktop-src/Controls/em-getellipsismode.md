---
title: EM_GETELLIPSISMODE Nachricht (Richedit.h)
description: Ruft den aktuellen Auslassungszeichenmodus ab.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE Windows-Steuerelemente
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
ms.openlocfilehash: 6706c2b6ee75852fd0b3ee7a1a9d18b25d20d242d72068ba073d1bb025ff8ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019698"
---
# <a name="em_getellipsismode-message"></a>EM \_ GETELLIPSISMODE-Nachricht

Ruft den aktuellen Auslassungszeichenmodus ab. Wenn diese Option aktiviert ist, wird eine Auslassungszeichen () für Text angezeigt, der nicht in das Anzeigefenster passt. Die Auslassungszeichen werden nur verwendet, wenn das Steuerelement nicht aktiv ist. Wenn aktiv, werden Bildlaufleisten verwendet, um Text anzuzeigen, der nicht in das Anzeigefenster passt.


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

Zeiger auf ein DWORD, das einen der folgenden Werte empfängt.



| Wert                                                                                                                                                         | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**AUSLASSUNGSZEICHEN \_ KEINE**</dt> </dl> | Es werden keine Auslassungszeichen verwendet.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**\_ELLIPSIS-ENDE**</dt> </dl>    | Auslassungszeichen am Ende (erzwungene Unterbrechung).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**WORT MIT DEN AUSLASSUNGSZEICHEN \_**</dt> </dl> | Auslassungszeichen am Ende (Wörterpause).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn wparam 0 und lparam nicht NULL ist, entspricht der Rückgabewert TRUE. Andernfalls entspricht der Rückgabewert FALSE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ SETELLIPSISMODE**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ GETELLIPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





