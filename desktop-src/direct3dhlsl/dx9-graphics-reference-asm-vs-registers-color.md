---
title: Farb Register
description: Diese Ausgabe Register des Vertex-Shader enthalten einen Farbwert.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350869"
---
# <a name="color-register"></a>Farb Register

Diese Ausgabe Register des Vertex-Shader enthalten einen Farbwert. 

| Register | BESCHREIBUNG              |
|----------|--------------------------|
| oD0      | diffuses Farbregister.  |
| oD1      | Glanz Farben Register. |



 

Der oD0-Wert wird interpoliert und in die Pixel-Shader-Farbregister 0 (V0) geschrieben. Der oD1-Wert wird interpoliert und in die Pixel-Shader-Farbregister 1 (v1) geschrieben. Weitere Informationen zu Pixel-Shader-Farb Registern finden Sie im Thema Pixel Shader- [Eingabe Farbregistrierung](dx9-graphics-reference-asm-ps-registers-input-color.md) .

## <a name="remarks"></a>Bemerkungen

Beispiel


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




