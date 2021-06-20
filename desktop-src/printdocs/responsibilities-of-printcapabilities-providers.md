---
description: PrintCapabilities-Anbieter müssen einen Mindestsatz von Funktionen unterstützen, die von der PrintTicket/PrintCapabilities-Anbieterschnittstelle impliziert werden.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Zuständigkeiten von PrintCapabilities-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404913"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="d65d3-103">Zuständigkeiten von PrintCapabilities-Anbietern</span><span class="sxs-lookup"><span data-stu-id="d65d3-103">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="d65d3-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="d65d3-104">This topic is not current.</span></span> <span data-ttu-id="d65d3-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="d65d3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d65d3-106">PrintCapabilities-Anbieter müssen einen Mindestsatz von Funktionen unterstützen, die von der PrintTicket/PrintCapabilities-Anbieterschnittstelle impliziert werden.</span><span class="sxs-lookup"><span data-stu-id="d65d3-106">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="d65d3-107">Diese Funktionen sind hier aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d65d3-107">These capabilities are listed here.</span></span>

-   <span data-ttu-id="d65d3-108">Sie müssen der Propagaterichtung folgen? XML-Attribut, wenn es im entsprechenden Kontext angezeigt wird und einen gültigen Wert für diesen Kontext enthält.</span><span class="sxs-lookup"><span data-stu-id="d65d3-108">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="d65d3-109">Sie müssen ein PrintCapabilities-Dokument generieren, das dem PrintCapabilities-Schema entspricht und die im Druckschema angegebenen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d65d3-109">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="d65d3-110">Sie müssen ein gültiges PrintTicket erkennen können.</span><span class="sxs-lookup"><span data-stu-id="d65d3-110">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="d65d3-111">Sie müssen in der Lage sein, ein PrintTicket zu interpretieren und die spezifische Konfiguration zu verstehen, die es darstellt.</span><span class="sxs-lookup"><span data-stu-id="d65d3-111">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="d65d3-112">Sie müssen ermitteln können, ob diese Konfiguration Einschränkungskonflikte enthält.</span><span class="sxs-lookup"><span data-stu-id="d65d3-112">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="d65d3-113">Sie müssen in der Lage sein, ein ungültiges oder in Konflikt stehende PrintTicket zu ändern, indem die am wenigsten signifikante Änderung erforderlich ist, um es sowohl gültig als auch konfliktfrei zu machen.</span><span class="sxs-lookup"><span data-stu-id="d65d3-113">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="d65d3-114">Sie müssen in der Lage sein, ein PrintCapabilities-Dokument für eine bestimmte Gerätekonfiguration zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d65d3-114">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="d65d3-115">Sie müssen in der Lage sein, eine Standardkonfiguration oder PrintTicket zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d65d3-115">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="d65d3-116">Sie müssen in der Lage sein, ein PrintCapabilities-Dokument zu generieren, das der Standardkonfiguration entspricht.</span><span class="sxs-lookup"><span data-stu-id="d65d3-116">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="d65d3-117">Sie müssen einen vom Gerätetreiber definierten Optionsbewertungsprozess implementieren, der in der Lage ist, die Nähe der Übereinstimmung zwischen zwei Optionsinstanzen zu bestimmen, die zum gleichen Feature gehören.</span><span class="sxs-lookup"><span data-stu-id="d65d3-117">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="d65d3-118">Dieser Algorithmus wird im PrintTicket-Überprüfungsprozess verwendet.</span><span class="sxs-lookup"><span data-stu-id="d65d3-118">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="d65d3-119">Zusätzlich zu den geltenden Anforderungen muss das PrintCapabilities-Dokument gültige und richtige Werte für jedes XML-Attribut (z. B. eingeschränkt) jeder Option enthalten.</span><span class="sxs-lookup"><span data-stu-id="d65d3-119">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d65d3-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d65d3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d65d3-121">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="d65d3-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



