---
description: Konstruktormethode.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Cbasevideorenderer. cbasevideorenderer-Konstruktor (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370109"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Cbasevideorenderer. cbasevideorenderer-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Renderclass* 
</dt> <dd>

Klassen Bezeichner für diesen Renderer.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Beschreibung, die für Debugzwecke verwendet wird.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf das aggregierte Besitzer Objekt.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




