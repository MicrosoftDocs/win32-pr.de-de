---
description: Vergleicht zwei Unicode-Zeichenfolgen, um zu bestimmen, ob eine Zeichenfolge ein Präfix der anderen ist.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: RtlPrefixUnicodeString-Funktion (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 28997f3bc85dedb9a18139cec13b9a76a8dd975e4ff57f1380053178bfaab328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076004"
---
# <a name="rtlprefixunicodestring-function"></a>RtlPrefixUnicodeString-Funktion

Vergleicht zwei Unicode-Zeichenfolgen, um zu bestimmen, ob eine Zeichenfolge ein Präfix der anderen ist.

## <a name="syntax"></a>Syntax


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*String1* \[ In\]
</dt> <dd>

Zeiger auf die erste Zeichenfolge, die möglicherweise ein Präfix der gepufferten Unicode-Zeichenfolge bei *String2* ist.

</dd> <dt>

*String2* \[ In\]
</dt> <dd>

Zeiger auf die zweite Zeichenfolge.

</dd> <dt>

*CaseInSensitive* \[ In\]
</dt> <dd>

True gibt an, dass der Fall beim Vergleich ignoriert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn *String1* ein Präfix von *String2* ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Ntddk.h (einschließlich Ntddk.h)</dt> </dl>                                    |
| Bibliothek<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




