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
ms.openlocfilehash: 123d4036713d6c1c5b7f7a08026d29d7d34126c28c5c2c1fceb94eb01baf9609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001240"
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

*szDllName* \[ In\]
</dt> <dd>

Der Name der DLL, die aus dem .NET Framework geladen werden soll.

</dd> <dt>

*szVersion* \[ In\]
</dt> <dd>

Die Version der zu ladenden DLL. Wenn *szVersion* **NULL** ist, wird die neueste Version der angegebenen DLL geladen.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Reserviert.

</dd> <dt>

*phModDll* \[ out\]
</dt> <dd>

Ein Handle für das Modul.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Funktion wird verwendet, um Bibliotheks-DLLs zu laden, die im .NET Framework verteilbaren Paket enthalten sind, nicht vom Benutzer generierte DLLs.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
