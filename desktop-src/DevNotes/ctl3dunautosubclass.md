---
description: Deaktiviert die automatische Unterklasse.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Ctl3dUnAutoSubclass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ca7980705ca93ad88b7c9e535abe59c3cdcc2e011130c843f0e89a533ce97599
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654470"
---
# <a name="ctl3dunautosubclass-function"></a>Ctl3dUnAutoSubclass-Funktion

Deaktiviert die automatische Unterklasse.

## <a name="syntax"></a>Syntax


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Funktion erfolgreich ist. andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
