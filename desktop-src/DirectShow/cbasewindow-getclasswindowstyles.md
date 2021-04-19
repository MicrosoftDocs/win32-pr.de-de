---
description: Die getclasswindowstyles-Methode ruft die Klassen Stile und Fenster Stile des Fensters ab.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Cbasewindow. getclasswindowstyles-Methode (winutil. h)
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
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370084"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>Cbasewindow. getclasswindowstyles-Methode

Die `GetClassWindowStyles` -Methode ruft die Klassen Stile und Fenster Stile des Fensters ab.

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

*pclassstyles* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Klassen Stile empfängt.

</dd> <dt>

*pwindowstyles* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Fenster Stile empfängt.

</dd> <dt>

*pwindowstylesex* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die erweiterten Fenster Stile empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine statische Text Zeichenfolge zurück, die den Klassennamen enthält.

## <a name="remarks"></a>Bemerkungen

Die [**cbasewindow::P Analyse Window**](cbasewindow-preparewindow.md) -Methode ruft diese Methode auf, um die Klassen Stile und Fenster Stile des Fensters abzurufen.

Diese Methode ist rein virtuell. Diese Klasse muss von der abgeleiteten Klasse implementiert werden. Das folgende Beispiel zeigt eine mögliche Implementierung:


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



Das-Objekt verwendet den Klassen Stil für den **lpszClassName** -Member einer WNDCLASS-Struktur, die an die **registerClass** -Funktion übergeben wird. Das-Objekt verwendet die Fenster Stile für den *dwExStyle* -Parameter und den *dwstyle* -Parameter **der Funktion "** -Funktion". Weitere Informationen finden Sie unter Platform SDK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




