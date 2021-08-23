---
title: EM_SETELLIPSISMODE (Richedit.h)
description: Diese Meldung legt den aktuellen Auslassungsmodus fest.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445172ea0a4ed4ef49e9a131db8d4357faaa5f7fef553169b7a8e1e795fd01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019478"
---
# <a name="em_setellipsismode-message"></a>EM \_ SETELLIPSISMODE-Meldung

Diese Meldung legt den aktuellen Auslassungsmodus fest. Wenn diese Option aktiviert ist, wird für Text, der nicht in das Anzeigefenster passt, ein Auslassungs- () angezeigt. Die Auslassungsellipse wird nur verwendet, wenn das Steuerelement nicht aktiv ist. Wenn sie aktiv sind, werden Bildlaufleisten verwendet, um Text anzuzeigen, der nicht in das Anzeigefenster passt.


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein DWORD, das einen der folgenden Werte empfängt.



| Wert                                                                                                                                                         | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**KEINE \_ AUSLASSUNGSELLIPSE**</dt> </dl> | Es werden keine Auslassungsellipse verwendet.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**\_AUSLASSUNGSENDE**</dt> </dl>    | Auslassungsellipse am Ende (erzwungene Unterbrechung).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**WORT MIT \_ AUSLASSUNGSELLIPSEN**</dt> </dl> | Auslassungsellipse am Ende (Wörterpause).<br/>   |



 

Die Bits für diese Werte passen alle in die **ELLIPSIS \_ MASK**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn wparam 0 ist und lparam einer der Werte in der obigen Tabelle ist, entspricht der Rückgabewert TRUE. andernfalls entspricht der Rückgabewert FALSE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETELLIPSISMODE**](em-getellipsismode.md)
</dt> <dt>

[**EM \_ GETELLIPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





