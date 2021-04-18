---
title: return-Anweisung
description: Eine Return-Anweisung signalisiert das Ende einer Funktion.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Return-Anweisung HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976193"
---
# <a name="return-statement"></a><span data-ttu-id="f3dba-104">return-Anweisung</span><span class="sxs-lookup"><span data-stu-id="f3dba-104">return Statement</span></span>

<span data-ttu-id="f3dba-105">Eine Return-Anweisung signalisiert das Ende einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="f3dba-105">A return statement signals the end of a function.</span></span>



|                   |
|-------------------|
| <span data-ttu-id="f3dba-106">Rückgabe \[ Wert \] ;</span><span class="sxs-lookup"><span data-stu-id="f3dba-106">return \[value\];</span></span> |



 

<span data-ttu-id="f3dba-107">Die einfachste Return-Anweisung gibt die Steuerung von der Funktion an das aufrufenden Programm zurück. Es wird kein Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3dba-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="f3dba-108">Eine Return-Anweisung kann jedoch einen oder mehrere Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f3dba-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="f3dba-109">In diesem Beispiel wird ein Literalwert zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="f3dba-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="f3dba-110">In diesem Beispiel wird das skalare Ergebnis eines Ausdrucks zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3dba-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="f3dba-111">In diesem Beispiel wird ein Vektor mit vier Komponenten zurückgegeben, der aus einer lokalen Variablen und einem Literalelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f3dba-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="f3dba-112">In diesem Beispiel wird ein Vektor mit vier Komponenten zurückgegeben, der aus dem Ergebnis erstellt wird, das von einer intrinsischen Funktion zurückgegeben wird, sowie Literalwerte.</span><span class="sxs-lookup"><span data-stu-id="f3dba-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="f3dba-113">Dieses Beispiel gibt eine-Struktur zurück, die mindestens ein-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="f3dba-113">This example returns a structure that contains one or more members.</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a><span data-ttu-id="f3dba-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f3dba-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3dba-115">Funktionen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3dba-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




