---
description: Die GetDllVersion-Funktion ruft die Versionsnummer von Cabinet.dll ab.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 14f2da8c6f8c786042c2abd5f41e02bdfab6f33d9b8aa42a5b5f90a6c4357103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390710"
---
# <a name="getdllversion-function"></a>GetDllVersion-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass ihr Verhalten nicht garantiert werden kann. \]

Die **GetDllVersion-Funktion** ruft die Versionsnummer von Cabinet.dll ab.

## <a name="syntax"></a>Syntax


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Versionsnummer der Datei (siehe [VERSIONINFO-Ressource](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
