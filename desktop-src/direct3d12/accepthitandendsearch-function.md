---
description: Wird in einem beliebigen Treffer-Shader verwendet, um einen Commit für den aktuellen Treffer durchzusetzen und dann nach weiteren Treffern für den Strahl zu suchen.
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
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343604"
---
# <a name="accepthitandendsearch-function"></a>AcceptHitAndEndSearch-Funktion

Wird in einem [beliebigen Treffer-Shader](any-hit-shader.md) verwendet, um einen Commit für den aktuellen Treffer durchzusetzen und dann nach weiteren Treffern für den Strahl zu suchen. Wenn ein Schnittstellen-Shader ausgeführt wird, wird die Ausführung angehalten.  Die Ausführung wird an den [nächstgelegenen Treffer-Shader](closest-hit-shader.md)weitergeleitet, sofern diese aktiviert ist, und der nächstgelegene Treffer wurde bisher aufgezeichnet.

## <a name="syntax"></a>Syntax

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Rückgabewert

**void**

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




