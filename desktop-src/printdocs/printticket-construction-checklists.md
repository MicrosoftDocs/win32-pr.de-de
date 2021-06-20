---
description: Erfahren Sie, wie der Autor eines PrintTicket-Clients Elementtypen verwenden kann, um ein PrintTicket zu erstellen, das Absichten für ein Gerät beschreibt.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Prüflisten für die PrintTicket-Konstruktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76d47911d0060cc6d06604bfaeaa4abcebd3daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405473"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="95974-103">Prüflisten für die PrintTicket-Konstruktion</span><span class="sxs-lookup"><span data-stu-id="95974-103">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="95974-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="95974-104">This topic is not current.</span></span> <span data-ttu-id="95974-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="95974-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="95974-106">In diesem Abschnitt wird veranschaulicht, wie der Autor eines PrintTicket-Clients die im Druckschemaframework definierten Elementtypen verwenden kann, um ein PrintTicket zu erstellen, das Absichten für ein Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="95974-106">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="95974-107">PrintTicket kann generisch (nicht an ein bestimmtes Gerät gebunden) oder gerätespezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="95974-107">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="95974-108">Die Semantik von PrintTicket wird ausführlicher dargestellt.</span><span class="sxs-lookup"><span data-stu-id="95974-108">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="95974-109">Darüber hinaus enthält dieser Abschnitt eine Übersicht über Konzepte und Terminologie, die in den nachfolgenden Abschnitten ausführlicher behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="95974-109">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="95974-110">Es gibt zwei grundlegend unterschiedliche Ansätze zum Erstellen eines PrintTickets.</span><span class="sxs-lookup"><span data-stu-id="95974-110">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="95974-111">Beide Ansätze können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95974-111">Either approach can be used.</span></span>

-   <span data-ttu-id="95974-112">Richten Sie printTicket auf ein unbekanntes oder generisches Gerät aus, indem [Sie ein generisches PrintTicket erstellen.](creating-a-generic-printticket.md)</span><span class="sxs-lookup"><span data-stu-id="95974-112">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="95974-113">Wenn Ihr primäres Ziel darin besteht, die Absicht des Endbenutzers beizubehalten, sollten Sie diesen Ansatz verwenden, indem Sie ein nicht validiertes generisches PrintTicket mit dem Dokument erstellen und speichern.</span><span class="sxs-lookup"><span data-stu-id="95974-113">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="95974-114">Richten Sie printTicket auf ein bestimmtes Gerät aus, indem [Sie einen Device-Specific PrintTicket erstellen.](creating-a-device-specific-printticket.md)</span><span class="sxs-lookup"><span data-stu-id="95974-114">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="95974-115">Wenn Sie mehr daran interessiert sind, alle Features eines bestimmten Geräts zu nutzen, sollten Sie diesen Ansatz verwenden, indem Sie ein PrintTicket für das jeweilige Gerät erstellen und das überprüfte PrintTicket mit dem Dokument speichern.</span><span class="sxs-lookup"><span data-stu-id="95974-115">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95974-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95974-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95974-117">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="95974-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



