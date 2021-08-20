---
description: Die HTMLValueToUnicode-Funktion konvertiert eine \_ UTF8-HTML-CP-Zeichenfolge in eine Unicode-Zeichenfolge.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: HTMLValueToUnicode-Funktion (Netmon.h)
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
ms.openlocfilehash: 39b7c05a20e07f406f4036659008ad68a40d25ecc6bca3f0600d121cf6557a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981386"
---
# <a name="htmlvaluetounicode-function"></a>HTMLValueToUnicode-Funktion

Die **HTMLValueToUnicode-Funktion** konvertiert eine \_ UTF8-HTML-CP-Zeichenfolge in eine Unicode-Zeichenfolge.

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

Bei der Eingabe ein Zeiger auf die html-Zeichenfolge, die von MCSVC bereitgestellt wird.

Bei der Ausgabe zeigert auf die konvertierte Unicode-Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt die Unicode-Entsprechung der Zeichenfolge zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




