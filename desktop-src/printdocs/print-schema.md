---
description: In dieser Übersicht werden das Druckschema und Links zu Referenzthemen zum Druckschema beschrieben. Das Druckschema enthält die Druckschemaschlüsselwörter und das Framework.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Legacy-Druckschemareferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407133"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="54540-104">Legacy-Druckschemareferenz</span><span class="sxs-lookup"><span data-stu-id="54540-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="54540-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="54540-105">This topic is not current.</span></span> <span data-ttu-id="54540-106">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="54540-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54540-107">Das Druckschema und die zugehörigen Technologien sind in Microsoft .NET Framework 3.0, Microsoft Windows Vista und späteren Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="54540-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="54540-108">Das Druckschema bietet ein XML-basiertes Format zum Ausdrücken und Organisieren einer großen Gruppe von Eigenschaften, die entweder ein Auftragsformat oder PrintCapabilities in einer hierarchisch strukturierten Weise beschreiben.</span><span class="sxs-lookup"><span data-stu-id="54540-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="54540-109">Das Druckschema ist ein Oberbegriff, der zwei Komponenten umfasst: die Print Schema Keywords und das Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="54540-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="54540-110">Das Dokument Print Schema Keywords ist ein öffentliches Schema, das einen Satz von Elementinstanzen definiert, die zum Beschreiben von Geräteattributen und zum Formatieren von Druckaufträgen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="54540-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="54540-111">Das Druckschemaframework ist ein öffentliches Schema, das eine hierarchisch strukturierte Auflistung von XML-Elementtypen definiert und angibt, wie die Elementtypen zusammen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="54540-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="54540-112">Die Print Schema Keywords und das Print Schema Framework bilden die Grundlage für zwei Druckschema-bezogene Technologien, das PrintCapabilities-Schema und das PrintTicket-Schema.</span><span class="sxs-lookup"><span data-stu-id="54540-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="54540-113">Beachten Sie, dass eines der Ziele des Druckschemas die Unterstützung von Schemaerweiterungen durch Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="54540-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="54540-114">Das heißt, anbieter sind nicht darauf beschränkt, nur die Eigenschaften-, Feature-, Options- oder ParameterInit-Instanzen zu verwenden, die in den Druckschemaschlüsselwörtern in den auf dem Druckschemaframework erstellten Technologien definiert sind.</span><span class="sxs-lookup"><span data-stu-id="54540-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="54540-115">Anbieterspezifische Elementinstanzen können in Elementinstanzen, die in den Schlüsselwörtern für Druckschemas definiert sind, frei interspersiert werden.</span><span class="sxs-lookup"><span data-stu-id="54540-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="54540-116">Die einzige Anforderung ist, dass anbieterspezifische (d. h. private) Eigenschafteninstanzen zu einem Namespace gehören müssen, der dem Anbieter eindeutig zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="54540-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="54540-117">Hintergrund des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="54540-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="54540-118">Print Schema-Related Technologies</span><span class="sxs-lookup"><span data-stu-id="54540-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="54540-119">Im Druckschema verwendete Begriffe</span><span class="sxs-lookup"><span data-stu-id="54540-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="54540-120">Syntax des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="54540-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="54540-121">Zusammenfassung der Elementtypen</span><span class="sxs-lookup"><span data-stu-id="54540-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="54540-122">Druckschemaframework</span><span class="sxs-lookup"><span data-stu-id="54540-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="54540-123">Öffentliche Schlüsselwörter für Das Schema drucken</span><span class="sxs-lookup"><span data-stu-id="54540-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="54540-124">PrintCapabilities-Schema und Dokumentkonstruktion</span><span class="sxs-lookup"><span data-stu-id="54540-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="54540-125">PrintTicket-Schema und Dokumentkonstruktion</span><span class="sxs-lookup"><span data-stu-id="54540-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="54540-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54540-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54540-127">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="54540-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



