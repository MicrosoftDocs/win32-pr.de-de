---
description: Dieser Artikel bietet Ihnen einen schnellen Einstieg in die Implementierung von PrintTicket und PrintCapabilities für Ihre Anwendung oder Ihren Gerätetreiber.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Schnellstartanleitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6060de551d3fb663e148cf80f661c4d517a51b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405313"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="1aad7-103">Schnellstartanleitung</span><span class="sxs-lookup"><span data-stu-id="1aad7-103">Quick Starter Guide</span></span>

<span data-ttu-id="1aad7-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1aad7-104">This topic is not current.</span></span> <span data-ttu-id="1aad7-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="1aad7-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1aad7-106">Diese Seite soll Ihnen einen schnellen Einstieg in die Implementierung von PrintTicket und PrintCapabilities für Ihre Anwendung oder Ihren Gerätetreiber bieten.</span><span class="sxs-lookup"><span data-stu-id="1aad7-106">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="1aad7-107">Wir empfehlen Ihnen zwar, die Spezifikation für das Druckschema vollständig zu lesen, aber diese Seite hilft Ihnen bei einem Einstieg in wichtige Bereiche, auf die Sie achten sollten.</span><span class="sxs-lookup"><span data-stu-id="1aad7-107">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="1aad7-108">Lesen Sie [print Schema-Related Technologies ,](print-schema-related-technologies.md) um einen Überblick über die Technologien PrintTicket und Print Capabilities zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1aad7-108">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="1aad7-109">Stellen Sie sicher, dass Sie die Zusammenfassung der [Elementtypen](summary-of-element-types.md) verstanden haben, die verwendet werden, um Druckschema-bezogene Technologien auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="1aad7-109">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="1aad7-110">PrintCapabilities-Dokumente und PrintTickets werden auf drei [Bereichspräfixebenen](scoping-prefix.md) definiert: Auftrag, Dokument und Seite.</span><span class="sxs-lookup"><span data-stu-id="1aad7-110">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="1aad7-111">Lesen der verschiedenen [XML-Attribute,](xml-attributes.md) die in verschiedenen Druckschema-Elementtypen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1aad7-111">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="1aad7-112">Lesen Sie die [Prüfliste für die Dokumentkonstruktion von PrintCapabilities](printcapabilities-document-construction-checklist.md) und das [bereitgestellte PrintCapabilities-Dokumentbeispiel.](printcapabilities-document-example.md)</span><span class="sxs-lookup"><span data-stu-id="1aad7-112">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="1aad7-113">Überprüfen Sie die [Prüflisten für die PrintTicket-Konstruktion und](printticket-construction-checklists.md) das bereitgestellte [PrintTicket-Beispiel.](printticket-example.md)</span><span class="sxs-lookup"><span data-stu-id="1aad7-113">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="1aad7-114">PrintTicket-Anbieter sollten auch die [Prüfliste für die PrintTicket-Überprüfung überprüfen,](printticket-validation-checklist.md) um die Konformität mit der PrintSchema-Spezifikation sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1aad7-114">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="1aad7-115">Überprüfen Sie sowohl [vom Benutzer konfigurierbare Elemente](user-configurable-elements.md) als auch von [Parameterdefinitionen](parameter-definitions.md) öffentliche Druckschemaschlüsselwörter, die in einem PrintCapabilities-Dokument enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="1aad7-115">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="1aad7-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1aad7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aad7-117">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="1aad7-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



