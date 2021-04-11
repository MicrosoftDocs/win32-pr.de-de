---
description: Eine-Aufzählung, mit der angegeben wird, warum ein Pixel abgelehnt wurde.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelkillreason-Enumeration
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
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341819"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Pixelkillreason-Enumeration

Eine-Aufzählung, mit der angegeben wird, warum ein Pixel abgelehnt wurde.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ None**  
Ein Wert, der angibt, dass das Pixel nicht zurückgewiesen wurde.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR- \_ shaderkill**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Shader nicht ausgeführt wurde.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ scissortest**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Scheren-Test fehlgeschlagen ist.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ Alpha Atest**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Alpha Test fehlgeschlagen ist.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR- \_ Schablonen Test**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Schablonen Test fehlgeschlagen ist.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR- \_ depthtest**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der tiefen Test fehlgeschlagen ist.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR- \_ notkompatibilität**  
Ein Wert, der angibt, dass der Pixel Verlauf nicht berechnet werden kann.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR- \_ Fehler**  
Ein Wert, der angibt, dass das Pixel aufgrund eines allgemeinen Fehlers abgelehnt wurde.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR- \_ noschnittmenge**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der Draw-Befehl das Pixel nicht schneidet.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR- \_ okkluded**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil das Zeichnen geokelt wurde.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ depthstenciltest**  
Ein Wert, der angibt, dass das Pixel zurückgewiesen wurde, weil der tiefen-und Schablonen Test fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



