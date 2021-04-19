---
description: Eine Matrix zum Transformieren von Objekt Raum in Raum.
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
ms.openlocfilehash: 613b4c403f235819845114e7019e07051a25ec80
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342986"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Eine Matrix zum Transformieren von Objekt Raum in Raum. Objekt-Space bezieht sich auf den Raum der aktuellen Beschleunigungs Struktur der untersten Ebene.

## <a name="syntax"></a>Syntax

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Bemerkungen

Die Matrix ist eine Umsetzung der **ObjectToWorld3x4** -Matrix.

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




