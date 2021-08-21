---
description: Gibt an, ob die angegebene Farbe eine spezielle Textfarbe ist.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: FSpecialTextIMEColorStyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fa964ba5d1020a5d9ba35b7359d81d965778b8a1e1f546a0a6cac19d2611ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017728"
---
# <a name="fspecialtextimecolorstyle-function"></a>FSpecialTextIMEColorStyle-Funktion

Gibt an, ob die angegebene Farbe eine spezielle Textfarbe ist.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
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

Gibt **TRUE zurück,** wenn die Farbe eine spezielle Textfarbe ist.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
