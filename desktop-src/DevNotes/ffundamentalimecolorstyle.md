---
description: Gibt an, ob die angegebene Farbe eine grundlegende Farbe ist.
ms.assetid: 9a06fadc-9b97-4f7d-9488-688b72d14bc5
title: Ffundamentalimecolorstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FFundamentalIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c7de1bf4ef84d159d673e1039ad6ea328153b216
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361942"
---
# <a name="ffundamentalimecolorstyle-function"></a>Ffundamentalimecolorstyle-Funktion

Gibt an, ob die angegebene Farbe eine grundlegende Farbe ist.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FFundamentalIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcolorstyle* \[ in\]
</dt> <dd>

Eine **imecolorsty** -Struktur, die von der [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -Funktion oder der [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Farbe eine grundlegende Farbe ist.

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

 

 
