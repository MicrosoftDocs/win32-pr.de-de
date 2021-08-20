---
description: Wird in einem beliebigen Treffer-Shader verwendet, um den aktuellen Treffer zu commiten und dann die Suche nach mehr Treffern für den Strahl zu beenden.
ms.assetid: ''
title: AcceptHitAndEndSearch-Funktion
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 35073145a9b9a4788c6aed3bbae0633f0a9f5b85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813036"
---
# <a name="accepthitandendsearch-function"></a>AcceptHitAndEndSearch-Funktion

Wird in einem [beliebigen Treffer-Shader verwendet,](any-hit-shader.md) um den aktuellen Treffer zu commiten und dann die Suche nach mehr Treffern für den Strahl zu beenden. Wenn ein Schnittpunkt-Shader ausgeführt wird, wird die Ausführung beendet.  Die Ausführung wird an den [nächstgelegenen Treffer-Shader](closest-hit-shader.md)übergibt, sofern aktiviert, mit dem bisher am nächsten aufgezeichneten Treffer.

## <a name="syntax"></a>Syntax

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Rückgabewert

**void**

## <a name="remarks"></a>Hinweise

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)



## <a name="see-also"></a>Siehe auch

* [DIRECT3D 12 raytracing HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
