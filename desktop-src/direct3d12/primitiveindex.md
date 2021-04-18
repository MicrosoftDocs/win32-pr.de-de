---
description: Ruft den automatisch generierten Index des primitiven innerhalb der Geometrie innerhalb der Beschleunigung der Beschleunigung-Struktur der untersten Ebene ab.
ms.assetid: ''
title: Primitiveingedex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrimitiveIndex
api_type:
- NA
ms.openlocfilehash: d6d1e8ba338a3fb567b583b42074210b514ef360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343989"
---
# <a name="primitiveindex-function"></a>Primitiveingedex-Funktion

Ruft den automatisch generierten Index des primitiven innerhalb der Geometrie innerhalb der Beschleunigung der Beschleunigung-Struktur der untersten Ebene ab.

## <a name="syntax"></a>Syntax

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>Bemerkungen

Bei **D3D12 \_ Raytracing \_ Geometry \_ Type- \_ Dreiecke** ist dies der Dreieck Index innerhalb des Geometry-Objekts.

Für den **D3D12 \_ Raytracing-Geometry- \_ \_ Typ \_ prozedurale \_ primitive \_ aabsb** ist dies der Index für das aabb-Array, das das Geometry-Objekt definiert.

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)

## <a name="see-also"></a>Siehe auch

* [Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
