---
description: Gibt an, ob die angegebene Farbe eine RGB-Farbe ist.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: Frgbimecolorstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: df11a2ad972791eaf7049bdef5fa927aaa4119da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368431"
---
# <a name="frgbimecolorstyle-function"></a>Frgbimecolorstyle-Funktion

Gibt an, ob die angegebene Farbe eine RGB-Farbe ist.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FRGBIMEColorStyle(
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

Gibt **true** zurück, wenn die Farbe eine RGB-Farbe ist.

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

 

 
