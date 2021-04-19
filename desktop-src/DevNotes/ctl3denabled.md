---
description: Überprüft, ob Steuerelemente 3D-Effekte verwenden können.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356036"
---
# <a name="ctl3denabled-function"></a>Ctl3dEnabled-Funktion

Überprüft, ob Steuerelemente 3D-Effekte verwenden können.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn Steuerelemente 3D-Effekte verwenden können. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

In Windows 4,0 oder höher geben **Ctl3dEnabled** und [**Ctl3dRegister**](ctl3dregister.md) **false** zurück.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
