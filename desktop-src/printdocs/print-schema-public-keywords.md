---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Öffentliche Schlüsselwörter des Druck Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106361136"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="efa19-104">Öffentliche Schlüsselwörter des Druck Schemas</span><span class="sxs-lookup"><span data-stu-id="efa19-104">Print Schema Public Keywords</span></span>

<span data-ttu-id="efa19-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="efa19-105">This topic is not current.</span></span> <span data-ttu-id="efa19-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="efa19-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="efa19-107">Im folgenden Abschnitt werden die öffentlichen Schlüsselwörter angegeben, die für das Druck Schema definiert sind.</span><span class="sxs-lookup"><span data-stu-id="efa19-107">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="efa19-108">Öffentliche Schlüsselwörter der Druck Schema Verwendung für Druckfunktionen</span><span class="sxs-lookup"><span data-stu-id="efa19-108">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="efa19-109">Unter den öffentlichen Schlüsselwörtern printfunktionen angegebene Schlüsselwörter können in einem Dokument mit Druckfunktionen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="efa19-109">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="efa19-110">Weitere Informationen dazu, wie diese Schlüsselwörter mit der Print-Funktions Technologie interagieren, finden Sie in [der Übersicht über den printfunktionalitäten](overview-of-the-printcapabilities.md) -Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="efa19-110">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="efa19-111">Öffentliche Schlüsselwörter für PrintTicket sollten nicht in einem Printworks-Dokument angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="efa19-111">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="efa19-112">Verwendung von öffentlichen Schlüsselwörtern des Druck Schemas für Print Ticket</span><span class="sxs-lookup"><span data-stu-id="efa19-112">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="efa19-113">Schlüsselwörter, die unter den öffentlichen Schlüsselwörtern von PrintTicket angegeben werden, können in einem PrintTicket</span><span class="sxs-lookup"><span data-stu-id="efa19-113">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="efa19-114">PrintTicket-Schlüsselwörter werden als Eigenschafts Elementtyp implementiert.</span><span class="sxs-lookup"><span data-stu-id="efa19-114">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="efa19-115">Weitere Informationen dazu, wie diese Schlüsselwörter mit der PrintTicket-Technologie interagieren, finden Sie im Abschnitt [Konfigurationsinformationen, die sich nicht auf Print-Funktionen beziehen](configuration-information-not-related-to-printcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="efa19-115">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="efa19-116">Schlüsselwörter, die unter den öffentlichen Schlüsselwörtern von Print-Funktionen angegeben werden, können in einem PrintTicket angezeigt werden, je nach der Implementierung des Print Ticket in einer Anwendung und/oder einem Treiber</span><span class="sxs-lookup"><span data-stu-id="efa19-116">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="efa19-117">Dies ermöglicht die Auswahl für Geräte Attribute, die im Dokument printfunktionen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="efa19-117">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="efa19-118">Weitere Informationen zur Interaktion zwischen den printfunktionalitäten-Schlüsselwörtern und dem PrintTicket finden Sie im Abschnitt " [PrintTicket](purpose-of-the-printticket.md) ".</span><span class="sxs-lookup"><span data-stu-id="efa19-118">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efa19-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="efa19-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efa19-120">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="efa19-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



