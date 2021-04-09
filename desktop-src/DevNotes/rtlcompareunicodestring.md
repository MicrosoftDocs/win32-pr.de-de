---
description: Vergleicht zwei Unicode-Zeichen folgen.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Rtlcompareunicodestring-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861056"
---
# <a name="rtlcompareunicodestring-function"></a>Rtlcompareunicodestring-Funktion

Vergleicht zwei Unicode-Zeichen folgen.

## <a name="syntax"></a>Syntax


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeichenfolge1* \[ in\]
</dt> <dd>

Zeiger auf die erste Zeichenfolge.

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

Ein Wert mit Vorzeichen, der die Ergebnisse des Vergleichs ergibt:



| Rückgabecode                                                                               | Beschreibung                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**Zins**</dt> </dl>       | *Zeichenfolge1* ist *Zeichenfolge2*.<br/>          |
| <dl> <dt>**< NULL**</dt> </dl>  | *Zeichenfolge1* ist kleiner als *Zeichenfolge2*.<br/>    |
| <dl> <dt>**> NULL**</dt> </dl> | *Zeichenfolge1* ist größer als *Zeichenfolge2*.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>WDM. h (Include WDM. h, ntddk. h oder ntifs. h)</dt> </dl>                   |
| Bibliothek<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rtlcomparestring**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[**Rtlequalstring**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
