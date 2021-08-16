---
title: Farbregister
description: Diese Vertex-Shader-Ausgaberegister enthalten einen Farbwert.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b19850985002ad9c36a6a6366f744106cb041db858f9df9b755996e114fdf6c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512286"
---
# <a name="color-register"></a>Farbregister

Diese Vertex-Shader-Ausgaberegister enthalten einen Farbwert. 

| Registrieren | BESCHREIBUNG              |
|----------|--------------------------|
| oD0      | Diffuses Farbregister.  |
| oD1      | Specular color register (Specular-Farbregister). |



 

Der oD0-Wert wird interpoliert und in das Farbregister 0 (v0) des Pixelshader geschrieben. Der oD1-Wert wird interpoliert und in das Farbregister 1 (v1) des Pixelshader geschrieben. Weitere Informationen zu Pixel-Shader-Farbregistern finden Sie im Thema [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) des Pixelshader.

## <a name="remarks"></a>Bemerkungen

Beispiel


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




