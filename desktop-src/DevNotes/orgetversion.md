---
description: Diese Funktion Ruft die Version der Offline Registrierungs Bibliothek ab.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Orgetversion-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371128"
---
# <a name="orgetversion-function"></a>Orgetversion-Funktion

Diese Funktion Ruft die Version der Offline Registrierungs Bibliothek ab.

## <a name="syntax"></a>Syntax


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwmajorversion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, um die Hauptversion der Offline Registrierungs Bibliothek zu erhalten. Bei der ersten Veröffentlichung der Bibliothek ist der Wert 1.

</dd> <dt>

*pdwminorversion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, um die neben Version der Offline Registrierungs Bibliothek zu erhalten. Bei der ersten Veröffentlichung der Bibliothek ist der Wert 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




