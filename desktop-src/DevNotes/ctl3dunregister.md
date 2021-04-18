---
description: Hebt die Registrierung einer Anwendung als Client von ctl3d auf.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365611"
---
# <a name="ctl3dunregister-function"></a>Ctl3dUnregister-Funktion

Hebt die Registrierung einer Anwendung als Client von ctl3d auf.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinstapp* 
</dt> <dd>

Ein Handle für die Anwendung, deren Registrierung als Client aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Registrierung der Anwendung als Client von ctl3d aufgehoben wird. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung, die ctl3d verwendet, sollte diese Funktion in WinMain aufruft.

3D-Effekte sind auf Systemen mit einer geringeren Auflösung als VGA nicht verfügbar.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
