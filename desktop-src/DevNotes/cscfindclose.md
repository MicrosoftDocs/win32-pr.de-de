---
description: Schließt ein Suchhandle.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: Cscfindclose-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354713"
---
# <a name="cscfindclose-function"></a>Cscfindclose-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Schließt ein Suchhandle.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hfind* \[ in\]
</dt> <dd>

Ein Suchhandle, das von der [**cscfindfirstfilew**](cscfindfirstfilew.md) -Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cscfindfirstfilew**](cscfindfirstfilew.md)
</dt> </dl>

 

 
