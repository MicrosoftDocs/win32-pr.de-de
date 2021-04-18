---
description: Wird von einem beliebigen Treffer-Shader aufgerufen, um den Treffer zu verwerfen und den Shader zu beenden.
ms.assetid: ''
title: IgnoreHit-Funktion
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343615"
---
# <a name="ignorehit-function"></a>IgnoreHit-Funktion

Wird von einem [beliebigen Treffer-Shader](any-hit-shader.md) aufgerufen, um den Treffer zu verwerfen und den Shader zu beenden. Die Treffer Suche wird fortgesetzt, ohne dass der Abstand und die Attribute für den aktuellen Treffer übertragen werden.  Der [**reporthit**](reporthit-function.md) -Befehl wird im [schnittsshader](intersection-shader.md)aufgerufen, falls vorhanden, gibt false zurück.  Alle Änderungen, die bis zu diesem Punkt in einem beliebigen Treffer-Shader an der Ray-Nutzlast vorgenommen werden, werden beibehalten.

## <a name="syntax"></a>Syntax

```
void IgnoreHit();

```


## <a name="return-value"></a>Rückgabewert

**void**

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)




## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




