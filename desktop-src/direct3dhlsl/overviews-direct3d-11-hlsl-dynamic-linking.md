---
title: Dynamisches Verknüpfen
description: Grafik Entwickler erstellen manchmal große, allgemeine Shader, die von einer Vielzahl von Szenen Elementen verwendet werden können.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710860"
---
# <a name="dynamic-linking"></a><span data-ttu-id="41f1d-103">Dynamisches Verknüpfen</span><span class="sxs-lookup"><span data-stu-id="41f1d-103">Dynamic Linking</span></span>

<span data-ttu-id="41f1d-104">Grafik Entwickler erstellen manchmal große, allgemeine Shader, die von einer Vielzahl von Szenen Elementen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="41f1d-104">Graphics developers sometimes create large, general-purpose shaders that can be used by a wide variety of scene items.</span></span> <span data-ttu-id="41f1d-105">Zur Laufzeit führt der Shader bedingt Code aus, der für die jeweilige Situation geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="41f1d-105">At runtime, the shader conditionally runs code appropriate for the given situation.</span></span> <span data-ttu-id="41f1d-106">Leider verwenden diese großen, allgemeinen Shader allgemeine Register (GPRS) ineffizient und können viel langsamer als kleinere, gezieltere Shader sein.</span><span class="sxs-lookup"><span data-stu-id="41f1d-106">Unfortunately, these large, general-purpose shaders use general-purpose registers (GPRs) inefficiently, and can be much slower than smaller, more targeted shaders.</span></span>

<span data-ttu-id="41f1d-107">Shader Model 5 löst dieses Leistungsproblem durch die Einführung dynamischer shaderverknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="41f1d-107">Shader model 5 addresses this performance problem by introducing dynamic shader linking.</span></span> <span data-ttu-id="41f1d-108">Dynamisches Verknüpfen trennt Shader-Code Fragmente mithilfe von Schnittstellen und virtuellen Funktionen und ermöglicht es der Anwendung, das zu verwendende Fragment zur zeichnungszeit auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="41f1d-108">Dynamic linking separates shader code fragments by using interfaces and virtual functions and allows the application to select the fragment to use at draw time.</span></span> <span data-ttu-id="41f1d-109">Dies verbessert die Leistung, indem nur der benötigte Shader-Code und nicht der gesamte große Shader für allgemeine Zwecke gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="41f1d-109">This improves performance by binding only the shader code needed and not the entire large, general-purpose shader.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="41f1d-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="41f1d-110">In This Section</span></span>



| <span data-ttu-id="41f1d-111">Element</span><span class="sxs-lookup"><span data-stu-id="41f1d-111">Item</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="41f1d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41f1d-112">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f1d-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Speichern von Variablen und Typen für die Freigabe von Shadern](storing-variables-and-types-for-shaders-to-share.md)</span><span class="sxs-lookup"><span data-stu-id="41f1d-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Storing Variables and Types for Shaders to Share](storing-variables-and-types-for-shaders-to-share.md)</span></span><br/> | <span data-ttu-id="41f1d-114">Beschreibt das Klassen Verknüpfungs Objekt zum Speichern von Variablen und Typen, die von mehreren Shadern gemeinsam genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="41f1d-114">Describes the class linkage object for storing variables and types that multiple shaders can share.</span></span><br/> |
| <span data-ttu-id="41f1d-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Schnittstellen und Klassen](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span><span class="sxs-lookup"><span data-stu-id="41f1d-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces and Classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span></span><br/>                                                                                                         | <span data-ttu-id="41f1d-116">Beschreibt die Verwendung von HLSL-Schnittstellen und-Klassen zum Implementieren dynamischer Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="41f1d-116">Describes using HLSL interfaces and classes to implement dynamic linking.</span></span><br/>                           |
| <span data-ttu-id="41f1d-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Einschränkungen der Schnittstellen Verwendung](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span><span class="sxs-lookup"><span data-stu-id="41f1d-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Interface Usage Restrictions](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span></span><br/>                                                                            | <span data-ttu-id="41f1d-118">Beschreibt Einschränkungen bei der Verwendung von-Schnittstellen im Shader-Code.</span><span class="sxs-lookup"><span data-stu-id="41f1d-118">Describes restrictions on the use of interfaces in shader code.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="41f1d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41f1d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f1d-120">HLSL</span><span class="sxs-lookup"><span data-stu-id="41f1d-120">HLSL</span></span>](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





