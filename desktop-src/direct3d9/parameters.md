---
description: Parameter sind Effekt Variablen.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parameter (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125582"
---
# <a name="parameters-direct3d-9"></a><span data-ttu-id="7b9e7-103">Parameter (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b9e7-103">Parameters (Direct3D 9)</span></span>

<span data-ttu-id="7b9e7-104">Parameter sind Effekt Variablen.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-104">Parameters are effect variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b9e7-105">Syntax</span></span>

<span data-ttu-id="7b9e7-106">*Verwendungstyp-ID* \[ : Ausdruck für *semantische* \] \[ < *Anmerkung (en)* > \] \[ =   \] ;</span><span class="sxs-lookup"><span data-stu-id="7b9e7-106">*usage type ID* \[: *semantic*\] \[<*annotation(s)*>\] \[= *expression*\];</span></span>

<span data-ttu-id="7b9e7-107">Parameter können von der Anwendung gelesen und mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-107">Parameters can be read from and written to by the application with [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>

<span data-ttu-id="7b9e7-108">Auf Parameter kann in Funktionen und in Techniken (insbesondere auf der rechten Seite von Zustands Zuweisungen) verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-108">Parameters can be referenced in functions and in techniques (specifically, in the right side of state assignments).</span></span>



| <span data-ttu-id="7b9e7-109">Element</span><span class="sxs-lookup"><span data-stu-id="7b9e7-109">Item</span></span>                                                                                 | <span data-ttu-id="7b9e7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b9e7-110">Description</span></span>                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9e7-111"><span id="usage"></span><span id="USAGE"></span>*ungs*</span><span class="sxs-lookup"><span data-stu-id="7b9e7-111"><span id="usage"></span><span id="USAGE"></span>*usage*</span></span><br/>                   | <span data-ttu-id="7b9e7-112">Bereich des Parameters.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-112">Scope of the parameter.</span></span> <span data-ttu-id="7b9e7-113">Weitere Informationen finden Sie unter [Verwendungen und Literale (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="7b9e7-113">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span><br/>                                                             |
| <span data-ttu-id="7b9e7-114"><span id="type"></span><span id="TYPE"></span>*Sorte*</span><span class="sxs-lookup"><span data-stu-id="7b9e7-114"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                      | <span data-ttu-id="7b9e7-115">Jeder gültige [Verweis für den HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) -Typ.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-115">Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span><br/>                                                                        |
| <span data-ttu-id="7b9e7-116"><span id="ID"></span><span id="id"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="7b9e7-116"><span id="ID"></span><span id="id"></span>*ID*</span></span><br/>                            | <span data-ttu-id="7b9e7-117">Eine eindeutige Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-117">A unique name.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="7b9e7-118"><span id="semantic"></span><span id="SEMANTIC"></span>*tischer*</span><span class="sxs-lookup"><span data-stu-id="7b9e7-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantic*</span></span><br/>          | <span data-ttu-id="7b9e7-119">Ein Tag, das folgende Bezeichnerregeln angibt, die in der Regel die Verwendung des Parameters angeben</span><span class="sxs-lookup"><span data-stu-id="7b9e7-119">A tag following identifier rules that typically indicates the usage of the parameter.</span></span> <span data-ttu-id="7b9e7-120">Muss ein bestimmter Typ sein.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-120">Must be a particular type.</span></span><br/>                                     |
| <span data-ttu-id="7b9e7-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anmerkungen*</span><span class="sxs-lookup"><span data-stu-id="7b9e7-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span></span><br/> | <span data-ttu-id="7b9e7-122">NULL oder mehr Teile Benutzer spezifischer Informationen.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-122">Zero or more pieces of user-specific information.</span></span> <span data-ttu-id="7b9e7-123">Kann ein beliebiger Typ sein.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-123">May be any type.</span></span> <span data-ttu-id="7b9e7-124">Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit Anmerkungen](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="7b9e7-124">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/> |
| <span data-ttu-id="7b9e7-125"><span id="expression"></span><span id="EXPRESSION"></span>*Begriff*</span><span class="sxs-lookup"><span data-stu-id="7b9e7-125"><span id="expression"></span><span id="EXPRESSION"></span>*expression*</span></span><br/>    | <span data-ttu-id="7b9e7-126">Initialisiert den Wert des Parameters.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-126">Initializes the parameter's value.</span></span> <span data-ttu-id="7b9e7-127">Weitere Informationen finden Sie unter [Ausdrücke (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="7b9e7-127">See [Expressions (Direct3D 9)](expressions.md).</span></span><br/>                                                                  |



 

<span data-ttu-id="7b9e7-128">Parameter können mit jedem gültigen [Verweis für den HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) -Ausdruck initialisiert werden, der auf einen Literalwert reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-128">Parameters can be initialized to any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) expression that reduces to a literal value.</span></span>

<span data-ttu-id="7b9e7-129">Parameter Werte werden nicht durch die Ausführung von Zustands Zuweisungs-oder Funktionsaufrufen geändert.</span><span class="sxs-lookup"><span data-stu-id="7b9e7-129">Parameter values are not changed by the execution of state assignment or function calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b9e7-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b9e7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b9e7-131">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="7b9e7-131">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
