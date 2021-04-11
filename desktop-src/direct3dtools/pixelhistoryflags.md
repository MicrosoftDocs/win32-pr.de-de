---
description: Eine Enumeration, die Flags enthält, die zum Beschreiben eines Pixel Verlaufs Ergebnisses verwendet werden. Siehe pixelhistoryoperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelhistoryflags-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124159"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>Pixelhistoryflags-Enumeration

Eine Enumeration, die Flags enthält, die zum Beschreiben eines Pixel Verlaufs Ergebnisses verwendet werden. Siehe pixelhistoryoperation.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF- \_ InitialValue**  
Ein Flag, das dem Anfangs Farbwert (vor dem Frame) entspricht.

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ Löschen**  
Ein Flag, das dem klaren Farbergebnis entspricht.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF- \_ Zeichnen**  
Ein Flag, das dem Ergebnis der Zeichnungs Farbe entspricht.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ finalvalue**  
Ein Flag, das dem Endergebnis der endgültigen Farbe entspricht.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ hascolor**  
Ein Flag, das entspricht, ob das Farbergebnis in der pixelhistoryoperation-Struktur vorhanden ist.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ hasbcolor**  
Ein Flag, das entspricht, ob das endgültige Puffer Farbergebnis in der pixelhistoryoperation-Struktur vorhanden ist.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF- \_ Fehler**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ vertexprocessingskipped**  
Nicht verwendet.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ modifyresource**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ cannotrunfulldepthstenciltest**  
Ein Flag, das entspricht, dass es nicht möglich ist, den tiefen-oder Schablonen Test auszuführen.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



