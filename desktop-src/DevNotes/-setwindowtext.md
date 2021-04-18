---
description: Ändert den Text der Titelleiste des angegebenen Fensters (sofern eine solche).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: _SetWindowText-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365630"
---
# <a name="_setwindowtext-function"></a>\_SetWindowText-Funktion

\[Diese Funktion ist ein Wrapper über die **SetWindowText** -Funktion. Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **SetWindowText** direkt aufrufen.\]

Ändert den Text der Titelleiste des angegebenen Fensters (sofern eine solche). Siehe [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).

## <a name="syntax"></a>Syntax


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
