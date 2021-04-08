---
description: Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der folgenden Syntax deklariert wird.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Syntax Syntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861767"
---
# <a name="annotation-syntax-direct3d-10"></a><span data-ttu-id="83c36-103">Syntax Syntax (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="83c36-103">Annotation Syntax (Direct3D 10)</span></span>

<span data-ttu-id="83c36-104">Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der folgenden Syntax deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="83c36-104">An annotation is a user-defined piece of information, declared with the following syntax.</span></span>



| <span data-ttu-id="83c36-105"><Wert des *DataType* - *namens*  =  ;...; ></span><span class="sxs-lookup"><span data-stu-id="83c36-105"><*DataType* *Name* = *Value*; ... ;></span></span> |
|--------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="83c36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83c36-106">Parameters</span></span>



| <span data-ttu-id="83c36-107">Element</span><span class="sxs-lookup"><span data-stu-id="83c36-107">Item</span></span>                                                                                                   | <span data-ttu-id="83c36-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83c36-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c36-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datentyp*</span><span class="sxs-lookup"><span data-stu-id="83c36-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="83c36-110">\[im- \] Datentyp, der einen beliebigen [skalaren HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) -Typ und den [Zeichen Folgentyp](../direct3dhlsl/dx-graphics-hlsl-scalar.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="83c36-110">\[in\] The data type, which includes any [scalar HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) type as well as the [string type](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span></span><br/> |
| <span data-ttu-id="83c36-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="83c36-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="83c36-112">\[in \] einer ASCII-Zeichenfolge, die den Namen der Anmerkung darstellt.</span><span class="sxs-lookup"><span data-stu-id="83c36-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="83c36-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Wert*</span><span class="sxs-lookup"><span data-stu-id="83c36-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="83c36-114">\[im \] Anfangswert der Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="83c36-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="83c36-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="83c36-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="83c36-116">\[in \] zusätzlichen Anmerkungen (Name-Wert-Paare).</span><span class="sxs-lookup"><span data-stu-id="83c36-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="83c36-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83c36-117">Remarks</span></span>

<span data-ttu-id="83c36-118">Sie können mehr als eine Anmerkung in den spitzen Klammern hinzufügen, die jeweils durch ein Semikolon voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="83c36-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="83c36-119">Die Effekt-Framework-APIs erkennen Anmerkungen für globale Variablen. alle anderen Anmerkungen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="83c36-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="83c36-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="83c36-120">Example</span></span>

<span data-ttu-id="83c36-121">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="83c36-121">Here are some examples.</span></span>


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a><span data-ttu-id="83c36-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83c36-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83c36-123">Syntax der Effekt Variablen</span><span class="sxs-lookup"><span data-stu-id="83c36-123">Effect Variable Syntax</span></span>](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
