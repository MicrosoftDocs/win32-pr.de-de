---
description: Erfahren Sie mehr über einige der Funktionen und Informationen, die das PrintCapabilities-Dokument nicht bereitstellen soll.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Was ein PrintCapabilities-Dokument nicht ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409893"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="2e85c-103">Was ein PrintCapabilities-Dokument nicht ist</span><span class="sxs-lookup"><span data-stu-id="2e85c-103">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="2e85c-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="2e85c-104">This topic is not current.</span></span> <span data-ttu-id="2e85c-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="2e85c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e85c-106">Es lohnt sich, einige der Funktionen und Informationen auflisten, die das PrintCapabilities-Dokument nicht bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="2e85c-106">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="2e85c-107">Ein PrintCapabilities-Dokument:</span><span class="sxs-lookup"><span data-stu-id="2e85c-107">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="2e85c-108">Stellt keine mehrwertigen (konfigurationsabhängigen) Daten dar.</span><span class="sxs-lookup"><span data-stu-id="2e85c-108">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="2e85c-109">Jedes PrintCapabilities-Dokument wird für eine bestimmte Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e85c-109">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="2e85c-110">Keine Eigenschaft oder ScoredProperty im Dokument kann einen Wert haben, der von der jeweiligen Konfiguration abhängt.</span><span class="sxs-lookup"><span data-stu-id="2e85c-110">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="2e85c-111">In der anfänglichen Schemaversion muss der PrintCapabilities-Anbieter die Eingabe PrintTicket verarbeiten und ein PrintCapabilities-Dokument erstellen, das Eigenschaftswerte enthält, die für die im PrintTicket angegebene Konfiguration geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="2e85c-111">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="2e85c-112">Enthält keine Einschränkungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="2e85c-112">Does not contain constraint information.</span></span>

    <span data-ttu-id="2e85c-113">Das PrintCapabilities-Dokument gibt nicht an, welche Konfigurationen zulässig und welche nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2e85c-113">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="2e85c-114">In der anfänglichen Schemaversion muss der PrintCapabilities-Anbieter alle Informationen speichern, die zum Überprüfen von Konfigurationen erforderlich sind, eine Methode zur Überprüfung der PrintTicket-Eingabe angeben und ein korrigiertes PrintTicket zurückgeben, wenn das angegebene PrintTicket gegen eine oder mehrere Einschränkungen verstößt.</span><span class="sxs-lookup"><span data-stu-id="2e85c-114">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="2e85c-115">Enthält keine dynamischen Geräteinformationen.</span><span class="sxs-lookup"><span data-stu-id="2e85c-115">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="2e85c-116">Es ist zu viel Aufwand für die Konstruktion des PrintCapabilities-Dokuments verbunden, damit es für sich schnell ändernde Statusinformationen verwendet werden kann, z. B. Freidruckebenen, Papier, das in jeder Tablettleiste verbleibt, oder Papierstaustatus.</span><span class="sxs-lookup"><span data-stu-id="2e85c-116">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e85c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e85c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e85c-118">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="2e85c-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



