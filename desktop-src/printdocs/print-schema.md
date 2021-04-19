---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Ältere Druck Schema Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363900"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="09fb5-104">Ältere Druck Schema Referenz</span><span class="sxs-lookup"><span data-stu-id="09fb5-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="09fb5-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="09fb5-105">This topic is not current.</span></span> <span data-ttu-id="09fb5-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="09fb5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="09fb5-107">Das Druck Schema und zugehörige Technologien sind in den Microsoft .NET Framework 3,0, Microsoft Windows Vista und späteren Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09fb5-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="09fb5-108">Das Druck Schema bietet ein XML-basiertes Format zum Ausdrücken und organisieren eines großen Satzes von Eigenschaften, die entweder ein Auftrags Format oder Print-Funktionen hierarchisch strukturiert beschreiben.</span><span class="sxs-lookup"><span data-stu-id="09fb5-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="09fb5-109">Beim Druck Schema handelt es sich um einen Oberbegriff, der zwei Komponenten, die Schlüsselwörter des Druck Schemas und das Druck Schema Framework umfasst.</span><span class="sxs-lookup"><span data-stu-id="09fb5-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="09fb5-110">Das Schlüsselwort des Print Schema-Schlüssel Worts ist ein öffentliches Schema, das einen Satz von Element Instanzen definiert, die zum Beschreiben von Geräte Attributen und zum Formatieren von Druckaufträgen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="09fb5-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="09fb5-111">Das Print Schema-Framework ist ein öffentliches Schema, das eine hierarchisch strukturierte Auflistung von XML-Elementtypen definiert, und gibt an, wie die Elementtypen gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="09fb5-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="09fb5-112">Die Druck Schema Schlüsselwörter und das Druck Schema-Framework bilden die Grundlage für zwei Druck Schema bezogene Technologien, das printforms-Schema und das PrintTicket-Schema.</span><span class="sxs-lookup"><span data-stu-id="09fb5-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="09fb5-113">Beachten Sie, dass eines der Ziele des Druck Schemas darin besteht, Schema Erweiterungen durch Anbieter zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="09fb5-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="09fb5-114">Das heißt, die Anbieter sind nicht auf die Verwendung von Eigenschaften, Features, Optionen oder parameterinit-Instanzen beschränkt, die in den Schlüsselwörtern des Print-Schemas in den Technologien definiert sind, die auf dem Print Schema-Framework basieren.</span><span class="sxs-lookup"><span data-stu-id="09fb5-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="09fb5-115">Anbieterspezifische Element Instanzen können innerhalb von Element Instanzen, die in den Schlüsselwörtern des Print-Schemas definiert sind, frei durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="09fb5-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="09fb5-116">Die einzige Voraussetzung ist, dass anbieterspezifische (private) Eigenschaften Instanzen zu einem Namespace gehören müssen, der dem Anbieter eindeutig zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="09fb5-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="09fb5-117">Hintergrund des Druck Schemas</span><span class="sxs-lookup"><span data-stu-id="09fb5-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="09fb5-118">Druck Schema-Related Technologien</span><span class="sxs-lookup"><span data-stu-id="09fb5-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="09fb5-119">Begriffe, die im Druck Schema verwendet werden</span><span class="sxs-lookup"><span data-stu-id="09fb5-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="09fb5-120">Syntax des Druck Schemas</span><span class="sxs-lookup"><span data-stu-id="09fb5-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="09fb5-121">Zusammenfassung der Element Typen</span><span class="sxs-lookup"><span data-stu-id="09fb5-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="09fb5-122">Print Schema Framework</span><span class="sxs-lookup"><span data-stu-id="09fb5-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="09fb5-123">Öffentliche Schlüsselwörter des Druck Schemas</span><span class="sxs-lookup"><span data-stu-id="09fb5-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="09fb5-124">Printfunktionalitäten-Schema und Dokument Erstellung</span><span class="sxs-lookup"><span data-stu-id="09fb5-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="09fb5-125">PrintTicket-Schema und Dokument Erstellung</span><span class="sxs-lookup"><span data-stu-id="09fb5-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="09fb5-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09fb5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09fb5-127">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="09fb5-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



