---
description: Bestimmt, ob Offlinedateien aktiviert ist.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: Csciscscenabled-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366828"
---
# <a name="csciscscenabled-function"></a>Csciscscenabled-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Bestimmt, ob Offlinedateien aktiviert ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Offlinedateien aktiviert ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cscquerydatabasestatus**](cscquerydatabasestatus.md)
</dt> </dl>

 

 
