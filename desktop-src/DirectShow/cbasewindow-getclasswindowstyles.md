---
description: Die GetClassWindowStyles-Methode ruft die Klassenstile und Fensterstile des Fensters ab.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: CBaseWindow.GetClassWindowStyles-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba7042069d4f1190a88b25ea4cc349e8230c149dd61d2d06fc91fa3439a9e55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074629"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>CBaseWindow.GetClassWindowStyles-Methode

Die `GetClassWindowStyles` -Methode ruft die Klassenstile und Fensterstile des Fensters ab.

## <a name="syntax"></a>Syntax


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pClassStyles* 
</dt> <dd>

Zeiger auf eine Variable, die die Klassenstile empfängt.

</dd> <dt>

*pWindowStyles* 
</dt> <dd>

Zeiger auf eine Variable, die die Fensterstile empfängt.

</dd> <dt>

*pWindowStylesEx* 
</dt> <dd>

Zeiger auf eine Variable, die die erweiterten Fensterstile empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine statische Textzeichenfolge zurück, die den Klassennamen enthält.

## <a name="remarks"></a>Hinweise

Die [**CBaseWindow::P repareWindow-Methode**](cbasewindow-preparewindow.md) ruft diese Methode auf, um die Klassen- und Fensterstile des Fensters abzurufen.

Diese Methode ist rein virtuell. die abgeleitete Klasse muss sie implementieren. Das folgende Beispiel zeigt eine mögliche Implementierung:


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



Das -Objekt verwendet den Klassenstil für den **lpszClassName-Member** einer WNDCLASS-Struktur, den es an die **RegisterClass-Funktion** übergibt. Das -Objekt verwendet die Fensterstile für die *Parameter dwExStyle* und *dwStyle* der **CreateWindowEx-Funktion.** Weitere Informationen finden Sie im Plattform-SDK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




