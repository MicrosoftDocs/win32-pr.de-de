---
description: Eine Enumeration, die angibt, warum ein Pixel abgelehnt wurde.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PIXELKILLREASON-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58ead08f81c8dee1644e431ae100c5100551e9907ab9a9d5bf00f6aae3532abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119324"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON-Enumeration

Eine Enumeration, die angibt, warum ein Pixel abgelehnt wurde.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ NONE**  
Ein -Wert, der angibt, dass das Pixel nicht abgelehnt wurde.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, weil der Shader nicht ausgeführt wurde.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, weil beim Scissor-Test ein Fehler aufgetreten ist.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, weil der Alphatest fehlgeschlagen ist.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, weil beim Schablonentest ein Fehler aufgetreten ist.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, weil der Tiefentest fehlgeschlagen ist.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
Ein -Wert, der angibt, dass der Pixelverlauf nicht berechnet werden kann.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**\_PKR-FEHLER**  
Ein -Wert, der angibt, dass das Pixel aufgrund eines allgemeinen Fehlers abgelehnt wurde.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOINTERSECTION**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, da der Zeichnen-Aufruf das Pixel nicht überschneidet.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ OCCLUDED**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, da das Zeichnen verdeckt wurde.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**  
Ein -Wert, der angibt, dass das Pixel abgelehnt wurde, weil der Tiefen- und Schablonentest fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



