---
description: Vergleicht zwei Unicode-Zeichen folgen, um zu bestimmen, ob eine Zeichenfolge ein Präfix der anderen ist.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Rtlprefixunicodestring-Funktion (ntddk. h)
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
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483134"
---
# <a name="rtlprefixunicodestring-function"></a>Rtlprefixunicodestring-Funktion

Vergleicht zwei Unicode-Zeichen folgen, um zu bestimmen, ob eine Zeichenfolge ein Präfix der anderen ist.

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

*Zeichenfolge1* \[ in\]
</dt> <dd>

Ein Zeiger auf die erste Zeichenfolge, die möglicherweise ein Präfix der gepufferten Unicode-Zeichenfolge in *Zeichenfolge2* ist.

</dd> <dt>

*Zeichenfolge2* \[ in\]
</dt> <dd>

Zeiger auf die zweite Zeichenfolge.

</dd> <dt>

*CaseInsensitive* \[ in\]
</dt> <dd>

**True** gibt an, dass die Groß-/Kleinschreibung beim Vergleich ignoriert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True** , wenn *Zeichenfolge1* ein Präfix von *Zeichenfolge2* ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Ntddk. h (einschließlich ntddk. h)</dt> </dl>                                    |
| Bibliothek<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rtlcompareunicodestring**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




