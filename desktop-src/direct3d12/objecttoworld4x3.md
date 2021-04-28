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
ms.openlocfilehash: bc91c6e98aceb13af3f589f873a4b96c2b1843c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098298"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Eine Matrix für die Transformation von Objektraum in Raum. Objektraum bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur auf unterer Ebene.

## <a name="syntax"></a>Syntax

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Bemerkungen

Die Matrix ist ein Teil der **ObjectToWorld3x4-Matrix.**

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




