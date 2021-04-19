---
description: Registriert eine Anwendung als Client von ctl3d.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361652"
---
# <a name="ctl3dregister-function"></a>Ctl3dRegister-Funktion

Registriert eine Anwendung als Client von ctl3d.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinstapp* 
</dt> <dd>

Ein Handle für die Anwendung, die als Client registriert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn 3D-Effekte aktiv sind. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung, die ctl3d verwendet, sollte diese Funktion in WinMain aufruft.

3D-Effekte sind auf Systemen mit einer geringeren Auflösung als VGA nicht verfügbar.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
