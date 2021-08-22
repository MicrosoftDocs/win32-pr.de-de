---
description: 'CBaseVideoRenderer.CBaseVideoRenderer-Konstruktor : Konstruktormethode.'
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: CBaseVideoRenderer.CBaseVideoRenderer-Konstruktor (Renbase.h)
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
ms.openlocfilehash: ec6a5e12d12b12f22cf1089d85ed4c07656da86cda071d8645355890996e2cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954759"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>CBaseVideoRenderer.CBaseVideoRenderer-Konstruktor

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

*RenderClass* 
</dt> <dd>

Klassenbezeichner für diesen Renderer.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Beschreibung, die zu Debugzwecken verwendet wird.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf das aggregierte Besitzerobjekt.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




