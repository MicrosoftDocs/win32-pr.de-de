---
description: Gibt die Version von CTL3D an, die derzeit ausgeführt wird.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Ctl3dGetVer-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: f29963020290686521d5e3bd165d2c8fac6e5e0c96f34552ad11f725d95567cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654500"
---
# <a name="ctl3dgetver-function"></a>Ctl3dGetVer-Funktion

Gibt die Version von CTL3D an, die derzeit ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der die Hauptversionsnummer im hohen Byte und die Nebenversionsnummer im niedrigen Byte enthält.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
