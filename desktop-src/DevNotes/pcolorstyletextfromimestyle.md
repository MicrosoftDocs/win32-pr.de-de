---
description: Ruft den textfarbstil des angegebenen Stils ab.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: Pcolorstyletextfromimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 791fdaca4a93b0a44099306b8ae14ae4d5cb11cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361596"
---
# <a name="pcolorstyletextfromimestyle-function"></a>Pcolorstyletextfromimestyle-Funktion

Ruft den textfarbstil des angegebenen Stils ab.

## <a name="syntax"></a>Syntax


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pimestyle* \[ in\]
</dt> <dd>

Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Zeiger auf eine **imecolorsty** -Struktur, die den textfarbstil darstellt.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

Die **imecolorsty** -Struktur ist wie folgt definiert:

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pimestylefromattr**](pimestylefromattr.md)
</dt> </dl>

 

 
