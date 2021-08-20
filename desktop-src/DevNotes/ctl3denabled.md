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
ms.openlocfilehash: 0d8a234736631517a0e77f5ab23f07688e3d80aa4c8b74a3b2ee51351beece90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654590"
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

Gibt **TRUE** zurück, wenn Steuerelemente 3D-Effekte verwenden können. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

In Windows 4.0 oder höher geben **Ctl3dEnabled** und [**Ctl3dRegister**](ctl3dregister.md) **FALSE** zurück.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
