---
description: Multipliziert erweiterte ganze Zahlen.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Rtlextendebug-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351275"
---
# <a name="rtlextendedintegermultiply-function"></a>Rtlextendebug-Funktion

\[Die **rtlextendedintegermultiplizieren** -Funktion wird exportiert, um vorhandene Treiber Binärdateien zu unterstützen, und ist veraltet. Um eine bessere Leistung zu erzielen, verwenden Sie die Compilerunterstützung für ganzzahlige Vorgänge mit 64 Bit.\]

Multipliziert erweiterte ganze Zahlen.

## <a name="syntax"></a>Syntax


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Multiplicand* \[ in\]
</dt> <dd>

Multiplikand.

</dd> <dt>

*Multiplikator* \[ in\]
</dt> <dd>

Multiplikator.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Multiplikations Ergebnisse zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
