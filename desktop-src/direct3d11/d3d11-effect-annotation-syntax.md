---
title: Syntax Syntax (Direct3D 11)
description: Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der in diesem Abschnitt beschriebenen Syntax deklariert wird.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948769"
---
# <a name="annotation-syntax-direct3d-11"></a><span data-ttu-id="964cf-103">Syntax Syntax (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="964cf-103">Annotation Syntax (Direct3D 11)</span></span>

<span data-ttu-id="964cf-104">Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der in diesem Abschnitt beschriebenen Syntax deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="964cf-104">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span>



| <span data-ttu-id="964cf-105"><*DataType* - *namens*  =  *Wert*; *...* ; ></span><span class="sxs-lookup"><span data-stu-id="964cf-105"><*DataType* *Name* = *Value*; *...* ;></span></span> |
|----------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="964cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="964cf-106">Parameters</span></span>



| <span data-ttu-id="964cf-107">Element</span><span class="sxs-lookup"><span data-stu-id="964cf-107">Item</span></span>                                                                                                   | <span data-ttu-id="964cf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="964cf-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="964cf-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datentyp*</span><span class="sxs-lookup"><span data-stu-id="964cf-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="964cf-110">\[im- \] Datentyp, der einen beliebigen [skalaren HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) -Typ und den [Zeichen Folgentyp](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar)enthält.</span><span class="sxs-lookup"><span data-stu-id="964cf-110">\[in\] The data type, which includes any [scalar HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) type as well as the [string type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span></span><br/> |
| <span data-ttu-id="964cf-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="964cf-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="964cf-112">\[in \] einer ASCII-Zeichenfolge, die den Namen der Anmerkung darstellt.</span><span class="sxs-lookup"><span data-stu-id="964cf-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="964cf-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Wert*</span><span class="sxs-lookup"><span data-stu-id="964cf-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="964cf-114">\[im \] Anfangswert der Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="964cf-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="964cf-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="964cf-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="964cf-116">\[in \] zusätzlichen Anmerkungen (Name-Wert-Paare).</span><span class="sxs-lookup"><span data-stu-id="964cf-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="964cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="964cf-117">Remarks</span></span>

<span data-ttu-id="964cf-118">Sie können mehr als eine Anmerkung in den spitzen Klammern hinzufügen, die jeweils durch ein Semikolon voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="964cf-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="964cf-119">Die Effekt-Framework-APIs erkennen Anmerkungen für globale Variablen. alle anderen Anmerkungen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="964cf-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="964cf-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="964cf-120">Example</span></span>

<span data-ttu-id="964cf-121">Hier einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="964cf-121">Here are some examples.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="964cf-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="964cf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="964cf-123">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="964cf-123">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="964cf-124">Syntax der Effekt Variablen</span><span class="sxs-lookup"><span data-stu-id="964cf-124">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

