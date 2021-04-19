---
description: Gibt an, ob die angegebene Farbe eine Windows-Farbe ist.
ms.assetid: 0d2b2039-938c-4f9d-8ddc-9eb711f55009
title: Funktion "Funktion"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FWinIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 28731672f5f1aff385f9051ba8b641b7cdcdf83c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357602"
---
# <a name="fwinimecolorstyle-function"></a>Funktion "Funktion"

Gibt an, ob die angegebene Farbe eine Windows-Farbe ist.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FWinIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcolorstyle* \[ in\]
</dt> <dd>

Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Farbe eine Windows-Farbe ist.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**Pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
