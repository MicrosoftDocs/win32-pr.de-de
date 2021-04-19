---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Zuständigkeiten von printfunktionalitäten-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370357"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="46aa1-104">Zuständigkeiten von printfunktionalitäten-Anbietern</span><span class="sxs-lookup"><span data-stu-id="46aa1-104">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="46aa1-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="46aa1-105">This topic is not current.</span></span> <span data-ttu-id="46aa1-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="46aa1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="46aa1-107">Printfunktionalitäten-Anbieter müssen einen minimalen Satz von Funktionen unterstützen, die von der PrintTicket/printfunktionalitäten-Anbieter Schnittstelle impliziert werden.</span><span class="sxs-lookup"><span data-stu-id="46aa1-107">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="46aa1-108">Diese Funktionen sind hier aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="46aa1-108">These capabilities are listed here.</span></span>

-   <span data-ttu-id="46aa1-109">Sie müssen die Richtung der propagieren? XML-Attribut, wenn es im entsprechenden Kontext angezeigt wird und einen gültigen Wert für diesen Kontext enthält.</span><span class="sxs-lookup"><span data-stu-id="46aa1-109">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="46aa1-110">Sie müssen ein printfunktionalitäten-Dokument generieren, das dem printfunktionalitäten-Schema entspricht und die im Druck Schema angegebenen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="46aa1-110">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="46aa1-111">Sie müssen in der Lage sein, ein gültiges PrintTicket zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="46aa1-111">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="46aa1-112">Sie müssen in der Lage sein, ein Print Ticket zu interpretieren und die spezifische Konfiguration zu verstehen, die Sie repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="46aa1-112">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="46aa1-113">Sie müssen in der Lage sein, zu bestimmen, ob diese Konfiguration Einschränkungs Konflikte enthält.</span><span class="sxs-lookup"><span data-stu-id="46aa1-113">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="46aa1-114">Sie müssen in der Lage sein, ein ungültiges oder in Konflikt stehender PrintTicket zu ändern, indem Sie die am wenigsten bedeutende Änderung vornehmen, damit Sie sowohl gültig als auch ohne Konflikte ist.</span><span class="sxs-lookup"><span data-stu-id="46aa1-114">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="46aa1-115">Sie müssen in der Lage sein, ein printfunktionalitäten-Dokument für eine bestimmte Gerätekonfiguration zu generieren.</span><span class="sxs-lookup"><span data-stu-id="46aa1-115">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="46aa1-116">Sie müssen in der Lage sein, eine Standardkonfiguration oder PrintTicket zu generieren.</span><span class="sxs-lookup"><span data-stu-id="46aa1-116">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="46aa1-117">Sie müssen in der Lage sein, ein printfunktionalitäten-Dokument zu generieren, das der Standardkonfiguration entspricht.</span><span class="sxs-lookup"><span data-stu-id="46aa1-117">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="46aa1-118">Sie müssen einen vom Gerätetreiber definierten Prozess zur Durchführung von Optionen implementieren, der die Übereinstimmung der Übereinstimmung zwischen zwei Options Instanzen, die zu derselben Funktion gehören, bestimmen können.</span><span class="sxs-lookup"><span data-stu-id="46aa1-118">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="46aa1-119">Dieser Algorithmus wird in der PrintTicket-Überprüfung verwendet.</span><span class="sxs-lookup"><span data-stu-id="46aa1-119">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="46aa1-120">Zusätzlich zu den vorstehenden Anforderungen muss das printfunktionalitäten-Dokument gültige und korrekte Werte für jedes XML-Attribut (z. b. "eingeschränkt") jeder Option enthalten.</span><span class="sxs-lookup"><span data-stu-id="46aa1-120">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46aa1-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46aa1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46aa1-122">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="46aa1-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



