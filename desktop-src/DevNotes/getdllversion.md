---
description: Die getdllversion-Funktion Ruft die Versionsnummer Cabinet.dll ab.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Getdllversion-Funktion
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
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351264"
---
# <a name="getdllversion-function"></a>Getdllversion-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass Ihr Verhalten nicht garantiert werden kann. \]

Die **getdllversion** -Funktion Ruft die Versionsnummer Cabinet.dll ab.

## <a name="syntax"></a>Syntax


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Versionsnummer der Datei (siehe [VERSIONINFO-Ressource](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dllgetversion**](dllgetversion.md)
</dt> </dl>

 

 
