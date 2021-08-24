---
description: Eine -Enum, die Flags enthält, die verwendet werden, um ein Pixelverlaufsergebnis zu beschreiben. Siehe PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PIXELHISTORYFLAGS-Enumeration
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
ms.openlocfilehash: 6ff4447bdf19342dd2932f5b93eaf2722072660ae5007b40747834d603a6c57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726680"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS-Enumeration

Eine -Enum, die Flags enthält, die verwendet werden, um ein Pixelverlaufsergebnis zu beschreiben. Siehe PixelHistoryOperation.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ INITIALVALUE**  
Ein Flag, das dem ursprünglichen Farbwert (vor dem Frame) entspricht.

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ CLEAR**  
Ein Flag, das dem Ergebnis der eindeutigen Farbe entspricht.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ DRAW**  
Ein Flag, das dem Zeichnen-Farbergebnis entspricht.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ FINALVALUE**  
Ein Flag, das dem endgültigen Farbergebnis entspricht.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**  
Ein Flag, das entspricht, ob das Farbergebnis in der PixelHistoryOperation-Struktur vorhanden ist.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**  
Ein Flag, das entspricht, ob das endgültige Pufferfarbergebnis in der PixelHistoryOperation-Struktur vorhanden ist.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**\_PHF-FEHLER**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**  
Wird nicht verwendet.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**  
Ein Flag, das entspricht, wenn der Tiefen- oder Schablonentest nicht ausgeführt werden kann.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



