---
description: Die GetPropertyText-Funktion gibt einen Zeiger auf den Eigenschaftstext zurück.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: GetPropertyText-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b92bf854dd4a3e678a4eb5524bd47412f012da87a007e960498d11d4bff91ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982054"
---
# <a name="getpropertytext-function"></a>GetPropertyText-Funktion

Die **GetPropertyText-Funktion** gibt einen Zeiger auf den Eigenschaftstext zurück.

## <a name="syntax"></a>Syntax


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame.

</dd> <dt>

*lpPI* \[ In\]
</dt> <dd>

Zeiger auf eine Eigenschafteninstanz.

</dd> <dt>

*szBuffer* \[ In\]
</dt> <dd>

Zeiger auf die Eigenschaftentextzeichenfolge.

</dd> <dt>

*BufferSize* \[ In\]
</dt> <dd>

Größe des Textzeichenfolgenpuffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Eigenschaftentext.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetPropertyText-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




