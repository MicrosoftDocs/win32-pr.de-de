---
description: 'WorldToObject3x4: Eine Matrix für die Transformation vom Weltraum in den Objektraum.'
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: cc7bf7dc2f06102b9b23eafd45655f12816c8359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105238"
---
# <a name="worldtoobject3x4"></a>WorldToObject3x4

Eine Matrix zum Transformieren vom Weltraum in den Objektraum. Objektbereich bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur der unteren Ebene.

## <a name="syntax"></a>Syntax

```
void WorldToObject3x4();

```




## <a name="remarks"></a>Bemerkungen

Die Matrix ist eine Füge der **WorldToObject4x3-Matrix.**

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




