---
description: Multipliziert erweiterte ganze Zahlen.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply-Funktion
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
ms.openlocfilehash: 0048da80026029274a89d089f5c232311a481a6010c0aad32d8b1a6ae6cc6786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571470"
---
# <a name="rtlextendedintegermultiply-function"></a>RtlExtendedIntegerMultiply-Funktion

\[Die **RtlExtendedIntegerMultiply-Funktion** wird zur Unterstützung vorhandener Treiberbinärdateien exportiert und ist veraltet. Um eine bessere Leistung zu erzielen, verwenden Sie die Compilerunterstützung für 64-Bit-Ganzzahlvorgänge.\]

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

*Multiplicand* \[ In\]
</dt> <dd>

Multiplicand.

</dd> <dt>

*Multiplikator* \[ In\]
</dt> <dd>

Multiplikator.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Multiplikationsergebnis zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
