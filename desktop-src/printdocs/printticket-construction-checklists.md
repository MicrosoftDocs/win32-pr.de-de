---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Checklisten für die PrintTicket-Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366565"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="19370-104">Checklisten für die PrintTicket-Erstellung</span><span class="sxs-lookup"><span data-stu-id="19370-104">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="19370-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="19370-105">This topic is not current.</span></span> <span data-ttu-id="19370-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="19370-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19370-107">In diesem Abschnitt wird veranschaulicht, wie der Autor eines PrintTicket-Clients die im Druckschema-Framework definierten Elementtypen verwenden kann, um ein Print Ticket zu erstellen, das Intents für ein Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="19370-107">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="19370-108">Print Ticket kann generisch (nicht an ein bestimmtes Gerät gebunden) sein, oder es kann gerätespezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="19370-108">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="19370-109">Die Semantik von PrintTicket wird ausführlicher dargestellt.</span><span class="sxs-lookup"><span data-stu-id="19370-109">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="19370-110">Darüber hinaus enthält dieser Abschnitt eine Übersicht über die Konzepte und die Terminologie, die in den nachfolgenden Abschnitten ausführlicher behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="19370-110">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="19370-111">Es gibt zwei grundlegende Vorgehensweisen zum Erstellen eines PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="19370-111">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="19370-112">Beide Ansätze können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19370-112">Either approach can be used.</span></span>

-   <span data-ttu-id="19370-113">Richten Sie das PrintTicket mit einem unbekannten oder generischen Gerät ein, indem Sie [ein allgemeines PrintTicket erstellen](creating-a-generic-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="19370-113">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="19370-114">Wenn Ihr Hauptziel darin besteht, die Absicht des Endbenutzers beizubehalten, sollten Sie diese Vorgehensweise durchführen, indem Sie ein nicht validiertes, generisches Print Ticket mit dem Dokument erstellen und speichern.</span><span class="sxs-lookup"><span data-stu-id="19370-114">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="19370-115">Richten Sie das PrintTicket für ein bestimmtes Gerät ein, indem Sie [eine Device-Specific PrintTicket erstellen](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="19370-115">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="19370-116">Wenn Sie mehr von allen Features profitieren möchten, die von einem bestimmten Gerät angeboten werden, sollten Sie diesen Ansatz verwenden, indem Sie ein Print Ticket für das jeweilige Gerät erstellen und das überprüfte PrintTicket mit dem Dokument speichern.</span><span class="sxs-lookup"><span data-stu-id="19370-116">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19370-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19370-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19370-118">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="19370-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



