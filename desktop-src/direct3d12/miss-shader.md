---
description: Ein Shader, der aufgerufen wird, wenn keine Strahlkreuzungen gefunden oder akzeptiert werden.
ms.assetid: ''
title: Miss-Shader
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 30f7ce32e66a19984ce43737d9fc9cae83652c851174d7db350ca34628a33033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850823"
---
# <a name="miss-shader"></a>Miss-Shader

Ein Shader, der aufgerufen wird, wenn keine Strahlkreuzungen gefunden oder akzeptiert werden. Dies ist für hintergrund- oder sky-Schattierungen nützlich.  Der Fehlshader kann [**CallShader**](callshader-function.md) und **TraceRay** verwenden, um weitere Arbeit zu planen.

Der Miss-Shader muss einen benutzerdefinierten nutzlasttypisierten Strukturparameter enthalten, der mit dem für [**TraceRay**](traceray-function.md)bereitgestellten übereinstimmt.


## <a name="shader-type-attribute"></a>Shadertypattribut


```
[shader("miss")]
```



## <a name="example"></a>Beispiel

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




