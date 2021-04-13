---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Kurzanleitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f3933cb59e270dd8ef2eff8d295d33ab1f9203
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351778"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="82cce-104">Kurzanleitung</span><span class="sxs-lookup"><span data-stu-id="82cce-104">Quick Starter Guide</span></span>

<span data-ttu-id="82cce-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="82cce-105">This topic is not current.</span></span> <span data-ttu-id="82cce-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="82cce-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="82cce-107">Diese Seite soll Ihnen einen schnellen Einstieg in die Implementierung von PrintTicket und Print-Funktionen für Ihre Anwendung oder Ihren Gerätetreiber verschaffen.</span><span class="sxs-lookup"><span data-stu-id="82cce-107">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="82cce-108">Wir empfehlen zwar, dass Sie die Druck Schema Spezifikation vollständig lesen, aber auf dieser Seite erhalten Sie einen schnell Einstieg in wichtige Bereiche, die Sie berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="82cce-108">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="82cce-109">Lesen Sie die [Druck Schema-Related Technologien](print-schema-related-technologies.md) , um Ihnen einen Überblick über die Technologien PrintTicket und Druckfunktionen zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="82cce-109">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="82cce-110">Stellen Sie sicher, dass Sie die [Zusammenfassung der Element Typen](summary-of-element-types.md) verstehen, die zum Ausdrücken von Druck Schema bezogenen Technologien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82cce-110">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="82cce-111">Printfunktionalitäten-Dokumente und-PrintTickets sind auf drei Ebenen mit [Präfix Präfix](scoping-prefix.md) , Auftrag, Dokument und Seite definiert.</span><span class="sxs-lookup"><span data-stu-id="82cce-111">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="82cce-112">Lesen Sie die verschiedenen [XML-Attribute](xml-attributes.md) , die in unterschiedlichen Druck Schema-Elementtypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82cce-112">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="82cce-113">Weitere Informationen finden Sie in der Prüfliste für die [Dokument Erstellung in printfunktionalitäten](printcapabilities-document-construction-checklist.md) und im bereitgestellten [printfunktionen](printcapabilities-document-example.md)</span><span class="sxs-lookup"><span data-stu-id="82cce-113">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="82cce-114">Überprüfen Sie die [PrintTicket-Konstruktions Checklisten](printticket-construction-checklists.md) und auch das bereitgestellte [PrintTicket-Beispiel](printticket-example.md) .</span><span class="sxs-lookup"><span data-stu-id="82cce-114">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="82cce-115">Print Ticket-Anbieter sollten auch die [PrintTicket](printticket-validation-checklist.md) -Überprüfungs Prüfliste prüfen, um die Konformität mit der PrintSchema-Spezifikation sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="82cce-115">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="82cce-116">Überprüfen Sie sowohl vom [benutzerkonfigurierbare Elemente](user-configurable-elements.md) als auch das Schema Schlüsselwort der [Parameter Definitionen](parameter-definitions.md) , die in einem printfunktionen</span><span class="sxs-lookup"><span data-stu-id="82cce-116">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="82cce-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82cce-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82cce-118">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="82cce-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



