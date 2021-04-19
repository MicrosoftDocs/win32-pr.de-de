---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Syntax des Druck Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350604"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="9dfe9-104">Syntax des Druck Schemas</span><span class="sxs-lookup"><span data-stu-id="9dfe9-104">Syntax of the Print Schema</span></span>

<span data-ttu-id="9dfe9-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-105">This topic is not current.</span></span> <span data-ttu-id="9dfe9-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9dfe9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9dfe9-107">Das Druck Schema wird in der XML-Syntax ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-107">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="9dfe9-108">Leser werden daher wahrscheinlich mit XML-Syntax und Begriffen wie Element, Elementtag, Element Inhalt, Attribut und Namespace vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-108">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="9dfe9-109">Das Print Schema-Framework besteht aus einer kleinen Anzahl von Elementtypen. Jeder Elementtyp dient einem bestimmten Zweck in den Technologien, die auf dem Druck Schema basieren.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-109">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="9dfe9-110">Element Typen werden durch Ihr XML-Elementtag unterschieden.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-110">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="9dfe9-111">Das Print Schema-Framework definiert die allgemeine Struktur und Organisation der abhängigen Technologien, indem für jeden Elementtyp angegeben wird, welche Elementtypen als untergeordnete Elemente zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-111">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="9dfe9-112">Viele Elementtypen unterscheiden sich von anderen Elementen desselben Typs durch das Name-Attribut, das eine bedeutende Rolle im Schema spielt.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-112">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="9dfe9-113">Das Name-Attribut dient zum Identifizieren von Instanzen der einzelnen Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-113">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="9dfe9-114">Die Schlüsselwörter des Druck Schemas definieren einen Satz von Werten für das Name-Attribut für viele der Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-114">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="9dfe9-115">In den meisten Fällen können Anbieter dem Name-Attribut eigene Werte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-115">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="9dfe9-116">Sie müssen nur sicherstellen, dass die Werte XML-QNames sind, die mit einem Namespace qualifiziert sind, der für den Anbieter eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="9dfe9-116">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dfe9-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9dfe9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dfe9-118">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9dfe9-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



