---
description: .
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab869be07e5578d265db2e8e85147c213e1e17e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218495"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="b3314-103">Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="b3314-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="b3314-104">Dieser Abschnitt bietet eine Übersicht über das Testen von Anwendungs Kompatibilitätsproblemen und das Beheben dieser Probleme in Webanwendungen für Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="b3314-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="b3314-105">In den folgenden Themen werden die Änderungen in Internet Explorer 8 sowie die Tools und Technologien beschrieben, um die Kompatibilität Ihrer Anwendung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="b3314-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="b3314-106">`Section`</span><span class="sxs-lookup"><span data-stu-id="b3314-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="b3314-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3314-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3314-108">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="b3314-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="b3314-109">Bietet einen Überblick über die Kompatibilitäts Aspekte von Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="b3314-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="b3314-110">Grundlegendes zu Herausforderungen der Anwendungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="b3314-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="b3314-111">Bietet Hintergrundinformationen zur Kompatibilität mit Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="b3314-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="b3314-112">Webstandards und Anwendungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="b3314-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="b3314-113">Bietet Hintergrundinformationen dazu, warum Webstandards wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="b3314-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="b3314-114">Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="b3314-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="b3314-115">Stellt aktuelle Informationen zu Entwurfs Updates bereit, die sich auf die Kompatibilität auswirken.</span><span class="sxs-lookup"><span data-stu-id="b3314-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="b3314-116">Beheben von Kompatibilitätsproblemen in Webanwendungen und Add-ons</span><span class="sxs-lookup"><span data-stu-id="b3314-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="b3314-117">Bietet Vorschläge zum Beheben von Kompatibilitätsproblemen mit Webanwendungen und Add-ons.</span><span class="sxs-lookup"><span data-stu-id="b3314-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="b3314-118">Tools zum Debuggen von Webanwendungen und Add-ons</span><span class="sxs-lookup"><span data-stu-id="b3314-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="b3314-119">Listet Tools auf, die zum Debuggen von Webanwendungen und Add-ons verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b3314-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="b3314-120">Anhang 1: Browser Änderungen von Internet Explorer 6 zu Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="b3314-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="b3314-121">Listet Änderungen von Microsoft Internet Explorer 6 zu Internet Explorer 8 auf.</span><span class="sxs-lookup"><span data-stu-id="b3314-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="b3314-122">Anhang 2: Test Skript Szenarien</span><span class="sxs-lookup"><span data-stu-id="b3314-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="b3314-123">Listet Empfohlene Szenarios zum Testen von-Standorten auf Kompatibilität auf.</span><span class="sxs-lookup"><span data-stu-id="b3314-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



