---
title: earlydepthstencil
description: Erzwingt tiefen Schablonen Tests, bevor ein Shader ausgeführt wird.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993183"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Erzwingt tiefen Schablonen Tests, bevor ein Shader ausgeführt wird.


```
earlydepthstencil   
```



## <a name="remarks"></a>Bemerkungen

Das Testen der tiefen Schablone erfolgt in der Regel während der Pixel Verarbeitung durch einen PixelShader. Durch das Erzwingen einer frühen Tiefe der Schablone werden die Tests vor der Ausführung des Shaders durchgeführt. der Zweck besteht darin, die Leistung pro Pixel zu verbessern, indem eine nicht benötigte Pixel Verarbeitung durchgeführt/reduziert/vermieden wird.

Eine Anwendung kann eine frühe tiefen Schablone durch Bereitstellen des-Attributs erzwingen, oder die Hardware kann frühe tiefen Tests ausführen, wenn keine tiefen Werte geschrieben werden und keine ungeordneten Zugriffs Vorgänge in einem Shader als Optimierung ausgeführt werden.

Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




