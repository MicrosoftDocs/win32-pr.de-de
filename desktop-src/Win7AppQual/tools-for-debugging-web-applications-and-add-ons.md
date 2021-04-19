---
description: .
ms.assetid: ECE4A9C6-8553-4718-AAFA-AC4D9924A786
title: Tools zum Debuggen von Webanwendungen und Add-Ons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb68485cd674266235d430d7d26b9a39e6fbec14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357122"
---
# <a name="tools-for-debugging-web-applications-and-add-ons"></a><span data-ttu-id="9ad94-103">Tools zum Debuggen von Webanwendungen und Add-Ons</span><span class="sxs-lookup"><span data-stu-id="9ad94-103">Tools for Debugging Web Applications and Add-Ons</span></span>

<span data-ttu-id="9ad94-104">Anstatt [Kompatibilitätsprobleme bei Webanwendungen und Add-ons zu beheben](remediating-web-applications-and-add-ons.md), können Sie die Webanwendung oder Website im Windows Internet Explorer 8-Standardmodus nativ ausführen lassen, indem Sie Ihren Code auf die neuesten Webstandards schreiben.</span><span class="sxs-lookup"><span data-stu-id="9ad94-104">Instead of [fixing compatibility issues in web applications and add-ons](remediating-web-applications-and-add-ons.md), you can make the web application or website work natively in Windows Internet Explorer 8 standards mode by writing your code to the most recent web standards.</span></span>

<span data-ttu-id="9ad94-105">Um Probleme in Ihrer Anwendung oder Website vollständig zu bewerten, sollten Sie die Ursache des Problems untersuchen.</span><span class="sxs-lookup"><span data-stu-id="9ad94-105">To fully assess any problems in your application or website, you should research the root cause of the problem.</span></span> <span data-ttu-id="9ad94-106">Das Internet Explorer-Team hat z. b. die Hauptursachen mithilfe des Entwicklertools ermittelt und mögliche Probleme logisch reduziert.</span><span class="sxs-lookup"><span data-stu-id="9ad94-106">For example, the Internet Explorer team determined root causes by using the Developer Tools and logically reducing possible issues.</span></span> <span data-ttu-id="9ad94-107">In den folgenden Abschnitten werden verschiedene Tools beschrieben, um den Debugprozess zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="9ad94-107">The following sections describe several tools to help simplify the debugging process.</span></span>



| <span data-ttu-id="9ad94-108">`Section`</span><span class="sxs-lookup"><span data-stu-id="9ad94-108">Section</span></span>                                                                                                                    | <span data-ttu-id="9ad94-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ad94-109">Description</span></span>                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad94-110">Microsoft Expression Web SuperPreview</span><span class="sxs-lookup"><span data-stu-id="9ad94-110">Microsoft Expression Web SuperPreview</span></span>](microsoft-expression-web-superpreview.md)                                         | <span data-ttu-id="9ad94-111">Ein eigenständiges visuelles Debugtool, das die Migration Ihrer Websites von Microsoft Internet Explorer 6 zu Windows Internet Explorer 7 oder Internet Explorer 8 schneller und einfacher macht.</span><span class="sxs-lookup"><span data-stu-id="9ad94-111">A stand-alone visual debugging tool that makes it faster and easier to migrate your sites from Microsoft Internet Explorer 6 to Windows Internet Explorer 7 or Internet Explorer 8.</span></span> |
| [<span data-ttu-id="9ad94-112">Internet Explorer-Kompatibilitätstest-Tool (Internet Explorer Compatibility Test Tool, IECTT)</span><span class="sxs-lookup"><span data-stu-id="9ad94-112">Internet Explorer Compatibility Test Tool (IECTT)</span></span>](inernet-explorer-compatibility-test-tool--iectt-.md)                  | <span data-ttu-id="9ad94-113">Eine Komponente des [Microsoft Anwendungskompatibilitäts-Toolkits](/windows-hardware/get-started/adk-install) , die Ihnen bei der Diagnose von Problemen in Ihren Webanwendungen helfen kann.</span><span class="sxs-lookup"><span data-stu-id="9ad94-113">A component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install) that can help you diagnose issues in your web applications.</span></span>       |
| [<span data-ttu-id="9ad94-114">Internet Explorer 8-Entwicklertools</span><span class="sxs-lookup"><span data-stu-id="9ad94-114">Internet Explorer 8 Developer Tools</span></span>](internet-explorer-8-developer-tools.md)                                             | <span data-ttu-id="9ad94-115">Die Entwicklertools, die in Internet Explorer 8 zum Debuggen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9ad94-115">The developer tools that are included in Internet Explorer 8 for debugging.</span></span>                                                                                                         |
| [<span data-ttu-id="9ad94-116">Internet Explorer 8-Kompatibilitäts-Assistent (Aggiorno)</span><span class="sxs-lookup"><span data-stu-id="9ad94-116">Internet Explorer 8 Compatibility Wizard (Aggiorno)</span></span>](inernet-explorer-8-compatibility-wizard--aggiorno-.md)              | <span data-ttu-id="9ad94-117">Ein Drittanbieter Tool, das Websites automatisch aktualisiert, sodass Sie in Internet Explorer 8 richtig gerenstet werden, ohne dass die Kompatibilität in älteren Browsern unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="9ad94-117">A third-party tool that automatically upgrades websites to render correctly in Internet Explorer 8 without breaking compatibility in older browsers.</span></span>                                |
| [<span data-ttu-id="9ad94-118">Tool für den webdebugger von "Tool"</span><span class="sxs-lookup"><span data-stu-id="9ad94-118">Fiddler Web Debugger Tool</span></span>](fiddler-web-debugger-tool.md)                                                                 | <span data-ttu-id="9ad94-119">Ein Drittanbieter Tool zum Erfassen von Netzwerk Datenverkehr zwischen dem Internet und den Testcomputern.</span><span class="sxs-lookup"><span data-stu-id="9ad94-119">A third-party tool for capturing network traffic between the Internet and test computers.</span></span>                                                                                           |
| [<span data-ttu-id="9ad94-120">Anwendungskompatibilitätstests mit Abbildern virtueller Computer</span><span class="sxs-lookup"><span data-stu-id="9ad94-120">Application Compatibility Testing Using Virtual PC Images</span></span>](application-compatibility-testing-using-virtual-pc-images.md) | <span data-ttu-id="9ad94-121">Virtual PC-Images, die Kompatibilitätstests vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="9ad94-121">Virtual PC images that simplify compatibility testing.</span></span>                                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="9ad94-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ad94-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ad94-123">Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="9ad94-123">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
