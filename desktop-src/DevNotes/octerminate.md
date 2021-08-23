---
description: Schließt den OC-Manager.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 399bdb936befb4f7ff45f9f5a3b132245b984bf2a5201ce054ee0fbeb50f5598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833350"
---
# <a name="octerminate-function"></a>OcTerminate-Funktion

Schließt den OC-Manager.

## <a name="syntax"></a>Syntax


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OcManagerContext* \[ in, out\]
</dt> <dd>

Enthält bei der Eingabe den Kontextzeiger des OC-Managers, der von [**OcInitialize zurückgegeben wird.**](ocinitialize.md) Empfängt bei der Ausgabe **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
