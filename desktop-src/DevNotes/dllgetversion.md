---
description: Die DllGetVersion-Funktion ruft die Versionsnummer der Cabinet.dll mithilfe der CABINETDLLVERSIONINFO-Struktur ab.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: DllGetVersion-Funktion
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
ms.openlocfilehash: 7671465d20987de9ebe526db5961513c81cea5b30d6ad095baf4d3df3d798194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654040"
---
# <a name="dllgetversion-function"></a>DllGetVersion-Funktion

\[Diese Funktion wird nicht mehr unterstützt, sodass ihr Verhalten nicht garantiert werden kann.\]

Die **DllGetVersion-Funktion** ruft die Versionsnummer der Cabinet.dll mithilfe der [**CABINETDLLVERSIONINFO-Struktur**](cabinetdllversioninfo.md) ab.

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

Zeiger auf die [**CABINETDLLVERSIONINFO-Struktur,**](cabinetdllversioninfo.md) die die Versionsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)
</dt> <dt>

[**GetDllVersion**](getdllversion.md)
</dt> </dl>

 

 
