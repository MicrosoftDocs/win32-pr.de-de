---
description: PrintCapabilities beschreibt die Konfigurationen oder Zustände, die auf einem Gerät verfügbar sind und häufig in einer Reihe verschiedener Konfigurationen platziert werden können.
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: Übersicht über printCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8f61d1ee4125a9a1ac5f9ddb07cf226cd7094e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408523"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="07226-103">Übersicht über printCapabilities</span><span class="sxs-lookup"><span data-stu-id="07226-103">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="07226-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="07226-104">This topic is not current.</span></span> <span data-ttu-id="07226-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="07226-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="07226-106">Die PrintCapabilities beschreiben die Konfigurationen oder Zustände, die auf einem Gerät verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="07226-106">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="07226-107">Ein Gerät, das von PrintCapabilities beschrieben wird, kann häufig in einer Reihe verschiedener Konfigurationen platziert werden.</span><span class="sxs-lookup"><span data-stu-id="07226-107">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="07226-108">Im Fall eines Druckgeräts umfassen typische Druckattribute Duplexdruck, Auflösung und Mediengröße.</span><span class="sxs-lookup"><span data-stu-id="07226-108">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="07226-109">Wenn das Gerät diese Attribute unterstützt, sind sie Teil der Konfiguration für dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="07226-109">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="07226-110">Der Benutzer wählt eine bestimmte Konfiguration aus, indem er jedem der verfügbaren Attribute einen bestimmten Wert zuweist. Beispiel: Duplex: OneSided, Auflösung: 600 dpi und MediaSize: Legal.</span><span class="sxs-lookup"><span data-stu-id="07226-110">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="07226-111">Die PrintCapabilities basieren auf dem Druckschemaframework, das die Elemente definiert, die in PrintCapabilities verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="07226-111">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="07226-112">Die Druckschemaschlüsselwörter definieren häufig verwendete Elementhierarchien oder Schlüsselwörter, um die Portabilität der Informationen und Absichten zwischen einzelnen Clients zu fördern.</span><span class="sxs-lookup"><span data-stu-id="07226-112">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="07226-113">Die Druckschemaschlüsselwörter ermöglichen jedoch auch private Erweiterungen, sodass PrintCapabilities an bestimmte Anforderungen angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="07226-113">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07226-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07226-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07226-115">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="07226-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



