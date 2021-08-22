---
description: Ruft den Hintergrundfarbstil des angegebenen Stils ab.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: PColorStyleBackFromIMEStyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 86f7c5774767cf410f67fe79a741872c32874cbb92aafcefc2b08dbdc2904989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386640"
---
# <a name="pcolorstylebackfromimestyle-function"></a>PColorStyleBackFromIMEStyle-Funktion

Ruft den Hintergrundfarbstil des angegebenen Stils ab.

## <a name="syntax"></a>Syntax


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pimestyle* \[ In\]
</dt> <dd>

Eine **IMESTYLE-Struktur,** die von der [**PIMEStyleFromAttr-Funktion zurückgegeben**](pimestylefromattr.md) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Zeiger auf eine **IMECOLORSTY-Struktur,** die den Hintergrundfarbstil darstellt.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

Die **IMECOLORSTY-Struktur** ist wie folgt definiert:

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
