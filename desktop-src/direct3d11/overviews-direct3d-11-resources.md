---
title: Ressourcen
description: In diesem Abschnitt werden die Aspekte von Direct3D 11-Ressourcen beschrieben.
ms.assetid: 5b8b1198-73ed-4058-9fc6-a1c43902d732
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9ed73d81d2521fe97b36e6bfc8d71e387f8c9c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039866"
---
# <a name="resources"></a><span data-ttu-id="db080-103">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db080-103">Resources</span></span>

<span data-ttu-id="db080-104">Ressourcen stellen Daten für die Pipeline bereit und definieren, was während der Szene gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="db080-104">Resources provide data to the pipeline and define what is rendered during your scene.</span></span> <span data-ttu-id="db080-105">Ressourcen können von ihren Spiel Medien geladen oder dynamisch zur Laufzeit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="db080-105">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="db080-106">In der Regel enthalten Ressourcen Textur Daten, Scheitelpunkt Daten und shaderdaten.</span><span class="sxs-lookup"><span data-stu-id="db080-106">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="db080-107">Die meisten Direct3D-Anwendungen erstellen und zerstören Ressourcen in der gesamten Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="db080-107">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span> <span data-ttu-id="db080-108">In diesem Abschnitt werden die Aspekte von Direct3D 11-Ressourcen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db080-108">This section describes aspects of Direct3D 11 resources.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="db080-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="db080-109">In this section</span></span>



| <span data-ttu-id="db080-110">Thema</span><span class="sxs-lookup"><span data-stu-id="db080-110">Topic</span></span>                                                                                             | <span data-ttu-id="db080-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db080-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db080-112">Einführung in eine Ressource in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="db080-112">Introduction to a Resource in Direct3D 11</span></span>](overviews-direct3d-11-resources-intro.md)<br/> | <span data-ttu-id="db080-113">In diesem Thema werden Direct3D-Ressourcen wie Puffer und Texturen vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="db080-113">This topic introduces Direct3D resources such as buffers and textures.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="db080-114">Ressourcentypen</span><span class="sxs-lookup"><span data-stu-id="db080-114">Types of Resources</span></span>](overviews-direct3d-11-resources-types.md)<br/>                        | <span data-ttu-id="db080-115">In diesem Thema werden die Arten von Ressourcen aus Direct3D 10 sowie neue Typen in Direct3D 11 beschrieben, einschließlich strukturierter Puffer und Beschreib barer Texturen und Puffer.</span><span class="sxs-lookup"><span data-stu-id="db080-115">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span><br/>                                                                       |
| [<span data-ttu-id="db080-116">Ressourcen Limits</span><span class="sxs-lookup"><span data-stu-id="db080-116">Resource Limits</span></span>](overviews-direct3d-11-resources-limits.md)<br/>                          | <span data-ttu-id="db080-117">Dieses Thema enthält eine Liste der Ressourcen, die von Direct3D 11 unterstützt werden (insbesondere auf [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) 11 oder 9. x).</span><span class="sxs-lookup"><span data-stu-id="db080-117">This topic contains a list of resources that Direct3D 11 supports (specifically [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11 or 9.x hardware).</span></span><br/>                                 |
| [<span data-ttu-id="db080-118">Unterressourcen</span><span class="sxs-lookup"><span data-stu-id="db080-118">Subresources</span></span>](overviews-direct3d-11-resources-subresources.md)<br/>                       | <span data-ttu-id="db080-119">In diesem Thema werden Textur-unter Ressourcen oder Teile einer Ressource beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db080-119">This topic describes texture subresources, or portions of a resource.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="db080-120">Puffer</span><span class="sxs-lookup"><span data-stu-id="db080-120">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)<br/>                                 | <span data-ttu-id="db080-121">Puffer enthalten Daten, die zum Beschreiben von Geometrie, Indizierung von Geometrie Informationen und shaderkonstanten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db080-121">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="db080-122">In diesem Abschnitt werden Puffer beschrieben, die in Direct3D 11 verwendet werden, sowie Links zu aufgabenbasierter Dokumentation für gängige Szenarien.</span><span class="sxs-lookup"><span data-stu-id="db080-122">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/> |
| [<span data-ttu-id="db080-123">Texturen</span><span class="sxs-lookup"><span data-stu-id="db080-123">Textures</span></span>](overviews-direct3d-11-resources-textures.md)<br/>                               | <span data-ttu-id="db080-124">In diesem Abschnitt werden die in Direct3D 11 verwendeten Texturen und Links zur aufgabenbasierten Dokumentation für gängige Szenarios beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db080-124">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="db080-125">Gleitkommaregeln</span><span class="sxs-lookup"><span data-stu-id="db080-125">Floating-point rules</span></span>](floating-point-rules.md)<br/>                                       | <span data-ttu-id="db080-126">Direct3D 11 unterstützt mehrere Gleit Komma Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="db080-126">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="db080-127">Alle Gleit Komma Berechnungen arbeiten unter einer definierten Teilmenge der IEEE 754 32-Bit-Gleit Komma Regeln mit einfacher Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="db080-127">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span><br/>                                               |
| [<span data-ttu-id="db080-128">Gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db080-128">Tiled resources</span></span>](tiled-resources.md)<br/>                                                 | <span data-ttu-id="db080-129">Gekachelte Ressourcen können sich als große logische Ressourcen vorstellen, die kleine Mengen an physischem Arbeitsspeicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="db080-129">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span><br/>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="db080-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db080-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db080-131">Programmieranleitung für Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="db080-131">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





