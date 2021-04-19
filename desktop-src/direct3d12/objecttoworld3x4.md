---
description: Eine Matrix zum Transformieren von Objekt Raum in Raum.
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
ms.openlocfilehash: 04f80dde64984010c6e015f6e885565396d3b9c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344821"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Eine Matrix zum Transformieren von Objekt Raum in Raum. Objekt-Space bezieht sich auf den Raum der aktuellen Beschleunigungs Struktur der untersten Ebene.

## <a name="syntax"></a>Syntax

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Bemerkungen

Die Matrix ist eine Umsetzung der **ObjectToWorld4x3** -Matrix.

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




