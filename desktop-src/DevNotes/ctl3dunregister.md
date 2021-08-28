---
description: Aufheben der Registrierung einer Anwendung als Client von CTL3D.
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
ms.openlocfilehash: 32a954efceba7400692ad92c91bedb47283587827739c19f23e7802e1481fbe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691500"
---
# <a name="ctl3dunregister-function"></a>Ctl3dUnregister-Funktion

Aufheben der Registrierung einer Anwendung als Client von CTL3D.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinstApp* 
</dt> <dd>

Ein Handle für die Anwendung, deren Registrierung als Client aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Registrierung der Anwendung als Client von CTL3D aufgehoben wurde. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Eine Anwendung, die CTL3D verwendet, sollte diese Funktion in WinMain aufrufen.

3D-Effekte sind auf Systemen mit einer geringeren VGA-Auflösung nicht verfügbar.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
