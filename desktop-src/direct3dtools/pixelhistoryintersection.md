---
description: Stellt Informationen zu einem bestimmten dar.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelhistoryschnittschnittstruktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346208"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span id="vspixengine.pixelhistoryintersection"></span>Pixelhistoryschnittschnittstruktur

Stellt Informationen zu einem bestimmten

## <a name="syntax"></a>Syntax


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a>Member

**Framezahl**  
Der Rahmen des Grafik Ereignisses mit diesem Vorgang.

**VEI**  
Die ID des Grafik Ereignisses, das diesem Vorgang zugeordnet ist.

**rendertargetptr**  
Das Renderziel, das ursprünglich (innerhalb der erfassten Anwendung) mit diesem Vorgang zugeordnet wurde.

**eventType**  
Die Art des Ereignisses, das diesem Vorgang zugeordnet ist (insbesondere, ob es sich bei diesem Ereignis um einen zeichnen-Befehl handelt).

**Punkt**  
Die Koordinaten des Pixels im Framebuffer.

**bassemblerstagegeneratesinstanceid**  
true, wenn der Eingabe Assembler Instanz-IDs generiert. andernfalls false.

**flags**  
Eine Kombination von pixelhistoryflags-Werten. Weitere Informationen finden Sie unter der pixelhistoryflags-Enumeration.

**"binitialred"**  
Frame Puffer: Wert der roten Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.

**binitialgrün**  
Frame Puffer: Wert der grünen Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.

**"binitialblue"**  
Frame Puffer: Wert der blauen Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.

**"binitialalpha"**  
Frame Puffer: Wert der Alpha Farbkomponente von Frame Puffer, bevor eine Pixel-Shader-Ausgabe zusammengeführt wird. Das heißt, am Anfang dieses Frames.

**Labelfbinitialred**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der roten Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.

**Labelfbinitialgreen**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.

**Labelfbinitialblue**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.

**Labelfbinitialalpha**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha-Farbkomponente des Frame Puffer vor jeder Pixel Schattierung zugeordnet ist. Das heißt, am Anfang dieses Frames.

**mit dem Namen**  
Frame Puffer: Wert der roten Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.

**bgrün**  
Frame Puffer: Wert der grünen Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.

**"f"**  
Frame Puffer: Wert der blauen Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.

**"f"**  
Frame Puffer: Wert der Alpha Farbkomponente von Frame Puffer, nachdem alle Pixel-Shader-Ausgaben zusammengeführt wurden. Das heißt, die endgültige framepufferfarbe.

**Labelfgezüchtet**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der roten Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.

**Labelfbgrün**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.

**Labelfbblue**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.

**Labelfbalpha**  
Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha Farbkomponente des Frame Puffer nach der gesamten Pixel Schattierung zugeordnet ist. Das heißt, die endgültige framepufferfarbe.

**pixelkillreason**  
Gibt den Grund an, warum der Farb Beitrag des Pixels abgebrochen wurde.

**HRESULT**  
Wenn ein Fehler aufgetreten ist, enthält das DirectX HRESULT, das den Fehler angibt.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



