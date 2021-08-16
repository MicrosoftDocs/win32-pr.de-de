---
description: Gibt an, ob ein nicht farbiger Stil einen Unterstreichungsstil aufgibt.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: FUlIMEStyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c53e48fbf2c607ee8a99c4f952cdb1bf9056826def452c42283dfd615392c4ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956099"
---
# <a name="fulimestyle-function"></a>FUlIMEStyle-Funktion

Gibt an, ob ein nicht farbiger Stil einen Unterstreichungsstil aufgibt.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pimestyle* \[ In\]
</dt> <dd>

Eine VON [**DER PIMEStyleFromAttr-Funktion zurückgegebene**](pimestylefromattr.md) **IMESTYLE-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn der Stil über einen Unterstreichungsstil verfügt.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
