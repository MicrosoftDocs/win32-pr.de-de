---
description: Lädt eine angegebene Version einer .NET Framework Bibliotheks-DLL.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365916"
---
# <a name="loadlibraryshim-function"></a>LoadLibraryShim-Funktion

Lädt eine angegebene Version einer .NET Framework Bibliotheks-DLL.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szDllName* \[ in\]
</dt> <dd>

Der Name der dll, die aus dem .NET Framework geladen werden soll.

</dd> <dt>

*szVersion* \[ in\]
</dt> <dd>

Die Version der zu ladenden DLL. Wenn *szVersion* **null** ist, wird die aktuelle Version der angegebenen DLL geladen.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Reserviert.

</dd> <dt>

*phModDll* \[ vorgenommen\]
</dt> <dd>

Ein Handle für das Modul.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird zum Laden von Bibliothek-DLLs verwendet, die in der .NET Framework weitervertreibbaren Pakets enthalten sind, nicht von benutzergenerierten DLLs.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
