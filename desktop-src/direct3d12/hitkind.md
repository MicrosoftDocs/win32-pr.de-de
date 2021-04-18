---
description: Gibt den Wert zurück, der als hitkind-Parameter an Report Thread übergeben wird.
ms.assetid: ''
title: Hitkind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345449"
---
# <a name="hitkind"></a>Hitkind

Gibt den Wert zurück, der als **hitkind** -Parameter an Report [**Thread**](reporthit-function.md)übergeben wird.

## <a name="syntax"></a>Syntax

```
uint HitKind();

```



## <a name="remarks"></a>Bemerkungen

Wenn die Schnittmenge von Dreiecks Schnittstellen mit fester Funktionsweise berichtet wurde, ist **hitkind** eines der **Treffer \_ Kind-Dreieck- \_ \_ Vorder \_** Seite (254) oder **Treffer Kind- \_ \_ Dreiecks \_ Rückseite \_** (255).

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




