---
description: 'ObjectToWorld4x3: Eine Matrix für die Transformation vom Objektraum in den Weltraum.'
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 22ad7bfafae89e33001d1d72878bc268ebfbd44649176b118a447fa16cf97d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608270"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Eine Matrix für die Transformation von Objektraum in Raum. Objektraum bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur auf unterer Ebene.

## <a name="syntax"></a>Syntax

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Hinweise

Die Matrix ist ein Teil der **ObjectToWorld3x4-Matrix.**

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




