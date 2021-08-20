---
description: Registriert eine Anwendung als Client von CTL3D.
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
ms.openlocfilehash: 9f58236891b8a673102905e0ef0c108ac9da6e6192788abea9c6e79baf8acfcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162158"
---
# <a name="ctl3dregister-function"></a>Ctl3dRegister-Funktion

Registriert eine Anwendung als Client von CTL3D.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinstApp* 
</dt> <dd>

Ein Handle für die Anwendung, die als Client registriert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn 3D-Effekte aktiv sind. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Eine Anwendung, die CTL3D verwendet, sollte diese Funktion in WinMain aufrufen.

3D-Effekte sind auf Systemen mit einer geringeren VGA-Auflösung nicht verfügbar.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
