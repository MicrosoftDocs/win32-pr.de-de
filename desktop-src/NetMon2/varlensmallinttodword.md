---
description: Die varlensmallinttodword-Funktion konvertiert eine kleine Ganzzahl variabler Länge in ein DWORD-Zeichen.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Varlensmallinttodword-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362411"
---
# <a name="varlensmallinttodword-function"></a>Varlensmallinttodword-Funktion

Die **varlensmallinttodword** -Funktion konvertiert eine kleine Ganzzahl variabler Länge in ein **DWORD**-Zeichen.

## <a name="syntax"></a>Syntax


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pValue* 
</dt> <dd>

Ein Zeiger auf die ganze Zahl mit variabler Länge.

</dd> <dt>

*Valuelen* 
</dt> <dd>

Länge (in Byte) der Variablen Länge, Small Integer.

</dd> <dt>

*fisbyteswgetauscht* 
</dt> <dd>

Flag, das angibt, ob die Länge der Variablen Länge kleiner als Byte ausgetauscht wird.

</dd> <dt>

*LPDWORD* 
</dt> <dd>

Das **DWORD** , in das die ganze Zahl konvertiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Zeiger auf das **DWORD**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




