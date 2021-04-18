---
description: An die traceray-Funktion übergeben, um den Ursprung, die Richtung und die Blöcke des Strahls zu definieren.
ms.assetid: ''
title: Rayde-Struktur
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
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345454"
---
# <a name="raydesc-structure"></a>Rayde-Struktur

An die [**traceray**](traceray-function.md) -Funktion übergeben, um den Ursprung, die Richtung und die Blöcke des Strahls zu definieren.

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

<span id="Origin"></span><span id="origin"></span>**Entstehungs**
</dt> <dd>

Der Ursprung des Strahls.

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**Tmin**
</dt> <dd>

Der minimale Umfang des Strahls.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Orientierung**
</dt> <dd>

Die Richtung des Strahls.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**TMAX**
</dt> <dd>

Der maximale Umfang des Strahls.


</dd>

## <a name="requirements"></a>Anforderungen



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




