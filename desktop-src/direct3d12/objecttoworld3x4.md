---
description: 'ObjectToWorld3x4: Eine Matrix für die Transformation vom Objektraum in den Weltraum.'
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: d58737e50fb7d173c84c4b38f6b91b9b6bfbc9d3b5a88c498344dadd5e94e73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123749"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Eine Matrix für die Transformation von Objektraum in Raum. Objektraum bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur auf unterer Ebene.

## <a name="syntax"></a>Syntax

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Hinweise

Die Matrix ist ein Teil der **ObjectToWorld4x3-Matrix.**

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




