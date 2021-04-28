---
description: 'ObjectToWorld3x4: Eine Matrix zum Transformieren vom Objektbereich in den Weltraum.'
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
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107738"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Eine Matrix zum Transformieren vom Objektraum in den Weltraum. Objektbereich bezieht sich auf den Raum der aktuellen Beschleunigungsstruktur der unteren Ebene.

## <a name="syntax"></a>Syntax

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Bemerkungen

Die Matrix ist eine Verwechsung der **ObjectToWorld4x3-Matrix.**

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




