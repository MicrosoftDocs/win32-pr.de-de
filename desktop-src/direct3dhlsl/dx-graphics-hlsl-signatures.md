---
title: Signaturen
description: Bei einer shadersignatur handelt es sich um eine Liste der Parameter, bei denen es sich entweder um Eingaben oder Ausgaben aus einer shaderfunktion handelt.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992855"
---
# <a name="signatures"></a><span data-ttu-id="21bfc-103">Signaturen</span><span class="sxs-lookup"><span data-stu-id="21bfc-103">Signatures</span></span>

<span data-ttu-id="21bfc-104">Bei einer shadersignatur handelt es sich um eine Liste der Parameter, bei denen es sich entweder um Eingaben oder Ausgaben aus einer shaderfunktion handelt.</span><span class="sxs-lookup"><span data-stu-id="21bfc-104">A shader signature is a list of the parameters that are either input to or output from a shader function.</span></span> <span data-ttu-id="21bfc-105">In Direct3D 10 Teilen angrenzende Stufen effektiv ein Register Array, bei dem der ausgabeshader (oder die Pipeline Phase) Daten an bestimmte Speicherorte im Register Array schreibt, und der Eingabe-Shader muss von denselben Speicherorten gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="21bfc-105">In Direct3D 10, adjacent stages effectively share a register array, where the output shader (or pipeline stage) writes data to specific locations in the register array and the input shader must read from the same locations.</span></span> <span data-ttu-id="21bfc-106">Die API verwendet shadersignaturen, um shaderausgaben ohne den Aufwand der semantischen Auflösung mit Eingaben zu binden.</span><span class="sxs-lookup"><span data-stu-id="21bfc-106">The API uses shader signatures to bind shader outputs with inputs without the overhead of semantic resolution.</span></span>

<span data-ttu-id="21bfc-107">In Direct3D 10 werden Eingabe Signaturen aus einer Shader-Input-Deklaration generiert, und die Ausgabe Signatur wird aus einer Shader-Output-Deklaration generiert.</span><span class="sxs-lookup"><span data-stu-id="21bfc-107">In Direct3D 10, input signatures are generated from a shader-input declaration and the output signature is generated from a shader-output declaration.</span></span> <span data-ttu-id="21bfc-108">Eine Eingabe Signatur ist mit einer Ausgabe Signatur kompatibel, wenn die Ausgabe Signatur eine strikte Teilmenge (Argumenttyp und Reihenfolge Übereinstimmung) der Eingabe Signatur ist.</span><span class="sxs-lookup"><span data-stu-id="21bfc-108">An input signature is said to be compatible with an output signature when the output signature is a strict subset (argument type and order match) of the input signature.</span></span> <span data-ttu-id="21bfc-109">Die einfachste Möglichkeit, dies zu erreichen, besteht darin, entsprechende shadereingaben und-Ausgaben mit dem gleichen Strukturtyp zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="21bfc-109">The most straightforward way to achieve this is to link corresponding shader inputs and outputs by the same structure type.</span></span>

<span data-ttu-id="21bfc-110">Im folgenden finden Sie ein Beispiel für kompatible Signaturen.</span><span class="sxs-lookup"><span data-stu-id="21bfc-110">Here is an example of compatible signatures.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



<span data-ttu-id="21bfc-111">Im folgenden finden Sie ein Beispiel für inkompatible Signaturen: die Reihenfolge der Parameter in der Eingabe Signatur entspricht nicht der Reihenfolge in der Ausgabe Signatur.</span><span class="sxs-lookup"><span data-stu-id="21bfc-111">Here is an example of incompatible signatures; the order of parameters in the input signature does not match the order in the output signature.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



<span data-ttu-id="21bfc-112">Psinworks ist eine kompatible Teilmenge von vsout (die ersten beiden Einträge entsprechen sowohl Typ als auch Order mit den ersten beiden Einträgen in vsout).</span><span class="sxs-lookup"><span data-stu-id="21bfc-112">PSInWorks is a compatible subset of VSOut (the first two entries match both type and order with the first two entries in VSOut).</span></span> <span data-ttu-id="21bfc-113">Psinmisslungen ist jedoch nicht kompatibel, da die Reihenfolge nicht mit vsout identisch ist.</span><span class="sxs-lookup"><span data-stu-id="21bfc-113">However, PSInFails is incompatible because the ordering does not match with VSOut.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21bfc-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21bfc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21bfc-115">Funktionen</span><span class="sxs-lookup"><span data-stu-id="21bfc-115">Functions</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




