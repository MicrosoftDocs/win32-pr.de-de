---
description: Gibt an, ob ein nicht farbiger Stil den italischen Stil auf hat.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: FItalicIMEStyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c8160edf46b97544ef27558bf15a8a58e447e78a0e0709432aea840f4567bc0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076114"
---
# <a name="fitalicimestyle-function"></a>FItalicIMEStyle-Funktion

Gibt an, ob ein nicht farbiger Stil den italischen Stil auf hat.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pimestyle* \[ In\]
</dt> <dd>

Eine VON [**der PIMEStyleFromAttr-Funktion zurückgegebene**](pimestylefromattr.md) **IMESTYLE-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn der Stil den italischen Stil hat.

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

 

 
