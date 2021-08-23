---
description: Gibt an, ob die angegebene Farbe eine spezielle Fensterfarbe ist.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: FSpecialWindowIMEColorStyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c42a8f4cf61b2b61d228dc243d06e902d825040570f4baa6502f2feba0322ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691340"
---
# <a name="fspecialwindowimecolorstyle-function"></a>FSpecialWindowIMEColorStyle-Funktion

Gibt an, ob die angegebene Farbe eine spezielle Fensterfarbe ist.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcolorstyle* \[ In\]
</dt> <dd>

Eine **IMECOLORSTY-Struktur,** die von einer [**PColorStyleBackFromIMEStyle-**](pcolorstylebackfromimestyle.md) oder [**PColorStyleTextFromIMEStyle-Funktion zurückgegeben**](pcolorstyletextfromimestyle.md) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Farbe eine spezielle Fensterfarbe (eine spezielle Farbe) ist.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
