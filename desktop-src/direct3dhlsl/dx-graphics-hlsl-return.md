---
title: return-Anweisung
description: Eine return-Anweisung signalisiert das Ende einer Funktion.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- return Statement HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119585"
---
# <a name="return-statement"></a><span data-ttu-id="bd19d-104">return-Anweisung</span><span class="sxs-lookup"><span data-stu-id="bd19d-104">return Statement</span></span>

<span data-ttu-id="bd19d-105">Eine return-Anweisung signalisiert das Ende einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="bd19d-105">A return statement signals the end of a function.</span></span>

<span data-ttu-id="bd19d-106">Rückgabewert \[ \] ;</span><span class="sxs-lookup"><span data-stu-id="bd19d-106">return \[value\];</span></span>



 

<span data-ttu-id="bd19d-107">Die einfachste return-Anweisung gibt die Steuerung von der Funktion an das aufrufende Programm zurück. gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd19d-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="bd19d-108">Eine return-Anweisung kann jedoch einen oder mehrere Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bd19d-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="bd19d-109">In diesem Beispiel wird ein Literalwert zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="bd19d-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="bd19d-110">In diesem Beispiel wird das skalare Ergebnis eines Ausdrucks zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd19d-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="bd19d-111">In diesem Beispiel wird ein Vektor mit vier Komponenten zurückgegeben, der aus einer lokalen Variablen und einem Literal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bd19d-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="bd19d-112">In diesem Beispiel wird ein Vierkomponentenvektor zurückgegeben, der aus dem Ergebnis erstellt wird, das von einer systeminternen Funktion zusammen mit Literalwerten zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd19d-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="bd19d-113">In diesem Beispiel wird eine -Struktur zurückgegeben, die einen oder mehrere Member enthält.</span><span class="sxs-lookup"><span data-stu-id="bd19d-113">This example returns a structure that contains one or more members.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="bd19d-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd19d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd19d-115">Funktionen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bd19d-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




