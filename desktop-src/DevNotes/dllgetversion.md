---
description: Die dllgetversion-Funktion Ruft die Versionsnummer Cabinet.dll mithilfe der cabinetdllversioninfo-Struktur ab.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: Dllgetversion-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367636"
---
# <a name="dllgetversion-function"></a>Dllgetversion-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass Ihr Verhalten nicht garantiert werden kann.\]

Die **dllgetversion** -Funktion Ruft die Versionsnummer Cabinet.dll mithilfe der [**cabinetdllversioninfo**](cabinetdllversioninfo.md) -Struktur ab.

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcdvi* 
</dt> <dd>

Ein Zeiger auf die [**cabinetdllversioninfo**](cabinetdllversioninfo.md) -Struktur, die die Versionsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cabinetdllversioninfo**](cabinetdllversioninfo.md)
</dt> <dt>

[**Getdllversion**](getdllversion.md)
</dt> </dl>

 

 
