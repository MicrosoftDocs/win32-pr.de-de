---
title: Effekt Gruppen Syntax (Direct3D 11)
description: Eine Effekt Gruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104472045"
---
# <a name="effect-group-syntax-direct3d-11"></a><span data-ttu-id="51fdd-103">Effekt Gruppen Syntax (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="51fdd-103">Effect Group Syntax (Direct3D 11)</span></span>

<span data-ttu-id="51fdd-104">Eine Effekt Gruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="51fdd-104">An effect group is declared with the syntax described in this section.</span></span>


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a><span data-ttu-id="51fdd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="51fdd-105">Parameters</span></span>



| <span data-ttu-id="51fdd-106">Element</span><span class="sxs-lookup"><span data-stu-id="51fdd-106">Item</span></span>                                                                                                                                                                           | <span data-ttu-id="51fdd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51fdd-107">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fdd-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span><span class="sxs-lookup"><span data-stu-id="51fdd-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span></span><br/>                                                                                                         | <span data-ttu-id="51fdd-109">erforderliche-Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="51fdd-109">equired keyword.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="51fdd-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span><span class="sxs-lookup"><span data-stu-id="51fdd-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span></span><br/>                                                                       | <span data-ttu-id="51fdd-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="51fdd-111">Required.</span></span> <span data-ttu-id="51fdd-112">Eine ASCII-Zeichenfolge, die den Namen der Effekt Gruppe eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51fdd-112">An ASCII string that uniquely identifies the name of the effect group.</span></span> <span data-ttu-id="51fdd-113">Anders als bei Techniken müssen Gruppen über Namen verfügen, um sicherzustellen, dass Techniken einen eindeutigen Bezeichner aufweisen (siehe Abschnitt "Gruppen und Techniken" weiter unten).</span><span class="sxs-lookup"><span data-stu-id="51fdd-113">Unlike techniques, groups must have names to ensure that techniques have a unique identifier (see Groups and Techniques section below).</span></span><br/> |
| <span data-ttu-id="51fdd-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Anmerkungen ></span><span class="sxs-lookup"><span data-stu-id="51fdd-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Annotations ></span></span><br/> | <span data-ttu-id="51fdd-115">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="51fdd-115">\[in\] Optional.</span></span> <span data-ttu-id="51fdd-116">Ein oder mehrere Teile der vom Benutzer bereitgestellten Informationen (Metadaten), die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="51fdd-116">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="51fdd-117">Informationen zur Syntax finden Sie unter Annotation-Syntax (Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="51fdd-117">For syntax, see Annotation Syntax (Direct3D 11).</span></span> <br/>                                                      |
| <span data-ttu-id="51fdd-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>Techniqueversion</span><span class="sxs-lookup"><span data-stu-id="51fdd-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/>                                           | <span data-ttu-id="51fdd-119">Entweder "technique10" oder "technique11".</span><span class="sxs-lookup"><span data-stu-id="51fdd-119">Either "technique10" or "technique11".</span></span> <span data-ttu-id="51fdd-120">Bei Techniken, die neue Funktionen für Direct3D 11 verwenden (5 \_ 0 Shader, bindinterfaces usw.), muss "technique11" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51fdd-120">Techniques which use functionality new to Direct3D 11 (5\_0 shaders, BindInterfaces, etc) must use "technique11".</span></span><br/>                                                                 |
| <span data-ttu-id="51fdd-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>Techniquename</span><span class="sxs-lookup"><span data-stu-id="51fdd-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span></span><br/>                                                       | <span data-ttu-id="51fdd-122">Optional.</span><span class="sxs-lookup"><span data-stu-id="51fdd-122">Optional.</span></span> <span data-ttu-id="51fdd-123">Eine ASCII-Zeichenfolge, die den Namen der Effekt Technik eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51fdd-123">An ASCII string that uniquely identifies the name of the effect technique.</span></span> <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a><span data-ttu-id="51fdd-124">Gruppen und Techniken</span><span class="sxs-lookup"><span data-stu-id="51fdd-124">Groups and Techniques</span></span>

<span data-ttu-id="51fdd-125">Um die Kompatibilität mit den Effekten von FX \_ 4 \_ 0 aufrechtzuerhalten, sind Gruppen optional.</span><span class="sxs-lookup"><span data-stu-id="51fdd-125">In order to maintain compatibility with fx\_4\_0 effects, groups are optional.</span></span> <span data-ttu-id="51fdd-126">Es gibt eine implizite Gruppe mit NULL-Namen, die alle globalen Techniken umfasst.</span><span class="sxs-lookup"><span data-stu-id="51fdd-126">There is an implicit NULL-named group surrounding all global techniques.</span></span>

<span data-ttu-id="51fdd-127">Betrachten Sie das folgende Beispiel:</span><span class="sxs-lookup"><span data-stu-id="51fdd-127">Consider the following example:</span></span>


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



<span data-ttu-id="51fdd-128">In C++ kann eine Technik anhand des Namens auf zwei Arten erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="51fdd-128">In C++, one can get a technique by name in two ways.</span></span> <span data-ttu-id="51fdd-129">Die folgenden Befehle werden die offensichtlichen Techniken finden:</span><span class="sxs-lookup"><span data-stu-id="51fdd-129">The following commands will find the obvious techniques:</span></span>


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



<span data-ttu-id="51fdd-130">Um sicherzustellen, dass [**ID3DX11Effect:: gettechniquebyname**](id3dx11effect-gettechniquebyname.md) ähnlich wie die Auswirkungen 10 funktioniert, müssen alle definierten Gruppen einen Namen haben.</span><span class="sxs-lookup"><span data-stu-id="51fdd-130">In order to ensure that [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) works similarly to Effects 10, all defined groups must have a name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51fdd-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51fdd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51fdd-132">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="51fdd-132">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="51fdd-133">Effekt Technik Syntax (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="51fdd-133">Effect Technique Syntax (Direct3D 11)</span></span>](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





