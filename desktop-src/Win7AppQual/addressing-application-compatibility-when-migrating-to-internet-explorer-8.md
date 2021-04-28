---
description: Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24fb4b0cbfb946f2385ddbd13ddc697987e659d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088768"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="31097-103">Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="31097-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="31097-104">Dieser Abschnitt bietet eine Übersicht über das Testen von Anwendungskompatibilitätsproblemen und das Beheben dieser Probleme in Webanwendungen für Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="31097-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="31097-105">In den folgenden Themen werden die Änderungen in Internet Explorer 8 und die Tools und Technologien beschrieben, um die Kompatibilität für Ihre Anwendung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="31097-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="31097-106">`Section`</span><span class="sxs-lookup"><span data-stu-id="31097-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="31097-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31097-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31097-108">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="31097-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="31097-109">Bietet eine Übersicht über überlegungen zur Kompatibilität Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="31097-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="31097-110">Grundlegendes zu Herausforderungen der Anwendungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="31097-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="31097-111">Stellt Hintergrundinformationen zur Kompatibilität von Internet Explorer 8 bereit.</span><span class="sxs-lookup"><span data-stu-id="31097-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="31097-112">Webstandards und Anwendungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="31097-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="31097-113">Bietet Hintergrundinformationen dazu, warum Webstandards wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="31097-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="31097-114">Entwurfsupdates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="31097-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="31097-115">Stellt unerzwehte Informationen zu Entwurfsupdates bereit, die sich auf die Kompatibilität auswirken.</span><span class="sxs-lookup"><span data-stu-id="31097-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="31097-116">Beheben von Kompatibilitätsproblemen in Webanwendungen und Add-Ons</span><span class="sxs-lookup"><span data-stu-id="31097-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="31097-117">Bietet Vorschläge zur Behandlung von Kompatibilitätsproblemen mit Webanwendungen und Add-Ons.</span><span class="sxs-lookup"><span data-stu-id="31097-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="31097-118">Tools zum Debuggen von Webanwendungen und Add-Ons</span><span class="sxs-lookup"><span data-stu-id="31097-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="31097-119">Listet Tools auf, die zum Debuggen von Webanwendungen und Add-Ons verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31097-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="31097-120">Anhang 1: Browseränderungen Internet Explorer 6 bis Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="31097-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="31097-121">Listet Änderungen von Microsoft Internet Explorer 6 in Internet Explorer 8 auf.</span><span class="sxs-lookup"><span data-stu-id="31097-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="31097-122">Anhang 2: Testskriptszenarien</span><span class="sxs-lookup"><span data-stu-id="31097-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="31097-123">Listet empfohlene Szenarien zum Testen von Standorten auf Kompatibilität auf.</span><span class="sxs-lookup"><span data-stu-id="31097-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



