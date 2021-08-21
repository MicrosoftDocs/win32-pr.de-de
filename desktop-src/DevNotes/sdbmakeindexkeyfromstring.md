---
description: Erstellt einen Schlüssel aus einer Zeichenfolge.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3298b0e038218aecb9676c596e7dbad09acbbdd4441d0f1cd79c3ec2a0188720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161223"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>SdbMakeIndexKeyFromString-Funktion

Erstellt einen Schlüssel aus einer Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszKey* \[ In\]
</dt> <dd>

Die Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt den Schlüssel oder 0 zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Hinweise

Der Standardindexschlüssel besteht aus den ersten acht Zeichen der Zeichenfolge, die in Großbuchstaben konvertiert und dann in einen **ULONGLONG-Wert** umgewandelt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




