---
description: Wird an die TraceRay-Funktion übergeben, um den Ursprung, die Richtung und die Umfang des Strahls zu definieren.
ms.assetid: ''
title: RayDesc-Struktur
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
ms.openlocfilehash: a4fa44e68e8747a0a8366ca2d949290f585d4b70d9e75b4ed2d3b6fdda0d05c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123685"
---
# <a name="raydesc-structure"></a>RayDesc-Struktur

Wird an die [**TraceRay-Funktion**](traceray-function.md) übergeben, um den Ursprung, die Richtung und die Umfang des Strahls zu definieren.

## <a name="syntax"></a>Syntax


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a>Felder

<dl> <dt>

<span id="Origin"></span><span id="origin"></span>**Ursprung**
</dt> <dd>

Der Ursprung des Strahls.

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**Tmin**
</dt> <dd>

Der minimale Umfang des Strahls.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Richtung**
</dt> <dd>

Die Richtung des Strahls.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**Tmax**
</dt> <dd>

Der maximale Umfang des Strahls.


</dd>

## <a name="requirements"></a>Anforderungen



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




