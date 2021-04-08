---
description: Die htmlvaluetounicode-Funktion konvertiert eine HTML CP- \_ UTF8-Zeichenfolge in eine Unicode-Zeichenfolge.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Htmlvaluetounicode-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750065"
---
# <a name="htmlvaluetounicode-function"></a>Htmlvaluetounicode-Funktion

Die **htmlvaluetounicode** -Funktion konvertiert eine HTML CP- \_ UTF8-Zeichenfolge in eine Unicode-Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pValue* \[ in, out\]
</dt> <dd>

Bei Eingabe ein Zeiger auf die HTML-Zeichenfolge, die von mcsvc bereitgestellt wird.

Bei Ausgabe, Zeiger auf die konvertierte Unicode-Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt die Unicode-Entsprechung der Zeichenfolge zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




