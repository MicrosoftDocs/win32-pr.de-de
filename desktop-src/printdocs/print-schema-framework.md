---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Print Schema Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219042"
---
# <a name="print-schema-framework"></a><span data-ttu-id="520c8-104">Print Schema Framework</span><span class="sxs-lookup"><span data-stu-id="520c8-104">Print Schema Framework</span></span>

<span data-ttu-id="520c8-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="520c8-105">This topic is not current.</span></span> <span data-ttu-id="520c8-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="520c8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="520c8-107">In diesem Abschnitt finden Sie ausführlichere Informationen zur Bedeutung und Verwendung der Druckschema-Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="520c8-107">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="520c8-108">Der Hauptschwerpunkt der ersten Version des Druck Schema-Frameworks ist das darstellen von Konfigurationen und Funktionen von Geräte Attributen.</span><span class="sxs-lookup"><span data-stu-id="520c8-108">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="520c8-109">Im großen Umfang bietet dieses Framework zwei unterschiedliche Arten der Beschreibung eines Geräte Attributs: als Funktions-/optionskonstrukt oder als Parameter Konstrukt.</span><span class="sxs-lookup"><span data-stu-id="520c8-109">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="520c8-110">Wenn ein Geräte Attribut über eine geringe Anzahl verfügbarer Werte oder Zustände verfügt, sollte das Attribut als Feature mit den zulässigen Werten oder Zuständen gekennzeichnet werden, die als Options Elemente bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="520c8-110">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="520c8-111">Wenn dagegen ein Geräte Attribut über eine große Anzahl verfügbarer Werte oder Zustände verfügt und der Satz aller möglichen Werte leicht definiert werden kann, ohne auf eine explizite Enumeration zurückgreifen zu müssen, sollte das Geräte Attribut als Parameter charakterisiert werden.</span><span class="sxs-lookup"><span data-stu-id="520c8-111">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="520c8-112">(Ein Parameter wird mithilfe eines ParameterDef-Elements definiert, und eine Parameter Instanz wird mithilfe eines parameterinit-Elements initialisiert.) Eigenschafts Elemente werden innerhalb von Feature/Option und parameterkonstrukten verwendet, um eine feinere Differenzierungs Ebene bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="520c8-112">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="520c8-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="520c8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="520c8-114">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="520c8-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



