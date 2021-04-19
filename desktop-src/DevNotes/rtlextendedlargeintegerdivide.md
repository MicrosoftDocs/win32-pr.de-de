---
description: Dividiert erweiterte ganze Zahlen.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: Rtlextende dlargeintegerdivide-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372164"
---
# <a name="rtlextendedlargeintegerdivide-function"></a>Rtlextende dlargeintegerdivide-Funktion

\[Die **rtlextendedlargeintegerdivide** -Funktion wird exportiert, um vorhandene Treiber Binärdateien zu unterstützen, und ist veraltet. Um eine bessere Leistung zu erzielen, verwenden Sie die Compilerunterstützung für ganzzahlige Vorgänge mit 64 Bit.\]

Dividiert erweiterte ganze Zahlen.

## <a name="syntax"></a>Syntax


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dividende* \[ in\]
</dt> <dd>

Dividend.

</dd> <dt>

*Divisor* \[ in\]
</dt> <dd>

Divisor.

</dd> <dt>

*Restwert* \[ in, out\]
</dt> <dd>

Zeiger auf Division Restwert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Ergebnis der Divisions Operation zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
