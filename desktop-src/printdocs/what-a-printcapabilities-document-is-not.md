---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Das Dokument "printfunktionalitäten" ist nicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353274"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="d799e-104">Das Dokument "printfunktionalitäten" ist nicht</span><span class="sxs-lookup"><span data-stu-id="d799e-104">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="d799e-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="d799e-105">This topic is not current.</span></span> <span data-ttu-id="d799e-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d799e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d799e-107">Es lohnt sich, einige der Funktionen und Informationen aufzulisten, die das Dokument printfunktionalitäten nicht bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="d799e-107">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="d799e-108">Ein printfunktionalitäten-Dokument:</span><span class="sxs-lookup"><span data-stu-id="d799e-108">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="d799e-109">Stellt keine mehrwertigen (Konfigurations abhängigen) Daten dar.</span><span class="sxs-lookup"><span data-stu-id="d799e-109">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="d799e-110">Jedes Dokument "printfunktionen" wird für eine bestimmte Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="d799e-110">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="d799e-111">Keine Eigenschaft oder ScoredProperty im Dokument kann über einen Wert verfügen, der von der jeweiligen Konfiguration abhängt.</span><span class="sxs-lookup"><span data-stu-id="d799e-111">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="d799e-112">In der anfänglichen Schema Version muss der PrintValues-Anbieter das PrintTicket-Eingabeverfahren verarbeiten und ein PrintValues-Dokument erstellen, das die für die im PrintTicket angegebenen Konfigurationen geeigneten Eigenschaftswerte enthält.</span><span class="sxs-lookup"><span data-stu-id="d799e-112">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="d799e-113">Enthält keine Einschränkungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="d799e-113">Does not contain constraint information.</span></span>

    <span data-ttu-id="d799e-114">Das Dokument printfunktionalitäten gibt nicht an, welche Konfigurationen zulässig sind und welche nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d799e-114">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="d799e-115">In der ersten Schema Version muss der printfunktionalitäten-Anbieter alle Informationen speichern, die zum Überprüfen von Konfigurationen erforderlich sind, eine Methode bereitstellen, die das PrintTicket-Eingabe Element überprüft, und ein korrigiertes Print Ticket zurückgeben, wenn das angegebene PrintTicket gegen eine oder mehrere Einschränkungen verstößt.</span><span class="sxs-lookup"><span data-stu-id="d799e-115">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="d799e-116">Enthält keine dynamischen Geräteinformationen.</span><span class="sxs-lookup"><span data-stu-id="d799e-116">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="d799e-117">Es ist zu viel mehr Aufwand bei der Erstellung des printfunktionalitäten-Dokuments, damit es für die schnelle Änderung von Statusinformationen verwendet werden kann, wie z. b. Freihand Ebenen, verbleibende Papier in jeder Info Leiste oder Papierstau Status.</span><span class="sxs-lookup"><span data-stu-id="d799e-117">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d799e-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d799e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d799e-119">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="d799e-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



