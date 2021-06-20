---
description: Erfahren Sie mehr über die Syntax des Druckschemas, das in XML-Syntax ausgedrückt wird und aus einer kleinen Anzahl von Elementtypen besteht.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Syntax des Druckschemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405293"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="e8f0c-103">Syntax des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e8f0c-103">Syntax of the Print Schema</span></span>

<span data-ttu-id="e8f0c-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-104">This topic is not current.</span></span> <span data-ttu-id="e8f0c-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="e8f0c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e8f0c-106">Das Druckschema wird in XML-Syntax ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-106">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="e8f0c-107">Daher wird erwartet, dass Leser mit xml-Syntax und Begriffen wie Element, Elementtag, Elementinhalt, Attribut und Namespace vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-107">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="e8f0c-108">Das Druckschemaframework besteht aus einer kleinen Anzahl von Elementtypen. Jeder Elementtyp erfüllt einen bestimmten Zweck in den Technologien, die auf dem Druckschema aufgebaut sind.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-108">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="e8f0c-109">Elementtypen werden durch ihr XML-Elementtag unterschieden.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-109">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="e8f0c-110">Das Druckschemaframework definiert die Gesamtstruktur und Organisation der abhängigen Technologien, indem für jeden Elementtyp angegeben wird, welche Elementtypen als untergeordnete Elemente zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-110">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="e8f0c-111">Viele Elementtypen unterscheiden sich durch das Namensattribut, das eine wichtige Rolle im Schema spielt, von anderen Elementtypen desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-111">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="e8f0c-112">Das Name-Attribut dient zum Identifizieren von Instanzen der einzelnen Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-112">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="e8f0c-113">Die Print Schema Keywords definiert einen Satz von Werten für das Name-Attribut für viele der Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-113">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="e8f0c-114">In den meisten Fällen können Anbieter dem Namensattribut eigene Werte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-114">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="e8f0c-115">Sie müssen nur sicherstellen, dass die Werte XML QNames sind, die mit einem Namespace qualifiziert sind, der für den Anbieter eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="e8f0c-115">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8f0c-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8f0c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f0c-117">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="e8f0c-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



