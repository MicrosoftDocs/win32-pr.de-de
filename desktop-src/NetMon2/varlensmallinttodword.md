---
description: Die VarLenSmallIntToDword-Funktion konvertiert eine kleine ganze Zahl variabler Länge in ein DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: VarLenSmallIntToDword-Funktion (Netmon.h)
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
ms.openlocfilehash: ffec440adc903ddb9a5157e8e5f36037e092f0c4bf0cd52da79b0839220366ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962730"
---
# <a name="varlensmallinttodword-function"></a>VarLenSmallIntToDword-Funktion

Die **VarLenSmallIntToDword-Funktion** konvertiert eine kleine ganze Zahl variabler Länge in einen **DWORD-Wert.**

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

*Pvalue* 
</dt> <dd>

Zeiger auf die kleine ganze Zahl variabler Länge.

</dd> <dt>

*ValueLen* 
</dt> <dd>

Länge (in Bytes) der variablen Länge, kleine ganze Zahl.

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Flag, das angibt, ob die kleine ganze Zahl variabler Länge bytegetauscht ist.

</dd> <dt>

*lpDword* 
</dt> <dd>

Das **DWORD,** in das die ganze Zahl konvertiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Zeiger auf **DWORD.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




