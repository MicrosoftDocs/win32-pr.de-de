---
description: Tools zum Debuggen von Webanwendungen und Add-Ons
ms.assetid: ECE4A9C6-8553-4718-AAFA-AC4D9924A786
title: Tools zum Debuggen von Webanwendungen und Add-Ons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fffe64836f6bce2b6e8b203360d0bba5b3872
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116078"
---
# <a name="tools-for-debugging-web-applications-and-add-ons"></a><span data-ttu-id="fefb6-103">Tools zum Debuggen von Webanwendungen und Add-Ons</span><span class="sxs-lookup"><span data-stu-id="fefb6-103">Tools for Debugging Web Applications and Add-Ons</span></span>

<span data-ttu-id="fefb6-104">Anstatt [Kompatibilitätsprobleme in Webanwendungen und Add-Ons](remediating-web-applications-and-add-ons.md)zu beheben, können Sie die Webanwendung oder Website nativ im Windows Internet Explorer 8-Standardmodus verwenden, indem Sie Ihren Code auf die neuesten Webstandards schreiben.</span><span class="sxs-lookup"><span data-stu-id="fefb6-104">Instead of [fixing compatibility issues in web applications and add-ons](remediating-web-applications-and-add-ons.md), you can make the web application or website work natively in Windows Internet Explorer 8 standards mode by writing your code to the most recent web standards.</span></span>

<span data-ttu-id="fefb6-105">Um Probleme in Ihrer Anwendung oder Website vollständig zu bewerten, sollten Sie die Grundursache des Problems untersuchen.</span><span class="sxs-lookup"><span data-stu-id="fefb6-105">To fully assess any problems in your application or website, you should research the root cause of the problem.</span></span> <span data-ttu-id="fefb6-106">Beispielsweise hat das Internet Explorer-Team die Grundursachen mithilfe der Entwicklertools ermittelt und mögliche Probleme logisch reduziert.</span><span class="sxs-lookup"><span data-stu-id="fefb6-106">For example, the Internet Explorer team determined root causes by using the Developer Tools and logically reducing possible issues.</span></span> <span data-ttu-id="fefb6-107">In den folgenden Abschnitten werden mehrere Tools beschrieben, um den Debugprozess zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="fefb6-107">The following sections describe several tools to help simplify the debugging process.</span></span>



| <span data-ttu-id="fefb6-108">`Section`</span><span class="sxs-lookup"><span data-stu-id="fefb6-108">Section</span></span>                                                                                                                    | <span data-ttu-id="fefb6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fefb6-109">Description</span></span>                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fefb6-110">Microsoft Expression Web SuperPreview</span><span class="sxs-lookup"><span data-stu-id="fefb6-110">Microsoft Expression Web SuperPreview</span></span>](microsoft-expression-web-superpreview.md)                                         | <span data-ttu-id="fefb6-111">Ein eigenständiges Visuelles Debugtool, mit dem Sie Ihre Websites schneller und einfacher von Microsoft Internet Explorer 6 zu Windows Internet Explorer 7 oder Internet Explorer 8 migrieren können.</span><span class="sxs-lookup"><span data-stu-id="fefb6-111">A stand-alone visual debugging tool that makes it faster and easier to migrate your sites from Microsoft Internet Explorer 6 to Windows Internet Explorer 7 or Internet Explorer 8.</span></span> |
| [<span data-ttu-id="fefb6-112">Internet Explorer-Kompatibilitätstest-Tool (Internet Explorer Compatibility Test Tool, IECTT)</span><span class="sxs-lookup"><span data-stu-id="fefb6-112">Internet Explorer Compatibility Test Tool (IECTT)</span></span>](inernet-explorer-compatibility-test-tool--iectt-.md)                  | <span data-ttu-id="fefb6-113">Eine Komponente des [Microsoft Application Compatibility Toolkit,](/windows-hardware/get-started/adk-install) mit der Sie Probleme in Ihren Webanwendungen diagnostizieren können.</span><span class="sxs-lookup"><span data-stu-id="fefb6-113">A component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install) that can help you diagnose issues in your web applications.</span></span>       |
| [<span data-ttu-id="fefb6-114">Internet Explorer 8-Entwicklertools</span><span class="sxs-lookup"><span data-stu-id="fefb6-114">Internet Explorer 8 Developer Tools</span></span>](internet-explorer-8-developer-tools.md)                                             | <span data-ttu-id="fefb6-115">Die Entwicklertools, die in Internet Explorer 8 für das Debuggen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fefb6-115">The developer tools that are included in Internet Explorer 8 for debugging.</span></span>                                                                                                         |
| [<span data-ttu-id="fefb6-116">Internet Explorer 8-Kompatibilitäts-Assistent (Aakurno)</span><span class="sxs-lookup"><span data-stu-id="fefb6-116">Internet Explorer 8 Compatibility Wizard (Aggiorno)</span></span>](inernet-explorer-8-compatibility-wizard--aggiorno-.md)              | <span data-ttu-id="fefb6-117">Ein Drittanbietertool, das Websites automatisch aktualisiert, sodass sie in Internet Explorer 8 ordnungsgemäß gerendert werden, ohne die Kompatibilität in älteren Browsern zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="fefb6-117">A third-party tool that automatically upgrades websites to render correctly in Internet Explorer 8 without breaking compatibility in older browsers.</span></span>                                |
| [<span data-ttu-id="fefb6-118">Fiddler-Webdebuggertool</span><span class="sxs-lookup"><span data-stu-id="fefb6-118">Fiddler Web Debugger Tool</span></span>](fiddler-web-debugger-tool.md)                                                                 | <span data-ttu-id="fefb6-119">Ein Drittanbietertool zum Erfassen von Netzwerkdatenverkehr zwischen dem Internet und Testcomputern.</span><span class="sxs-lookup"><span data-stu-id="fefb6-119">A third-party tool for capturing network traffic between the Internet and test computers.</span></span>                                                                                           |
| [<span data-ttu-id="fefb6-120">Anwendungskompatibilitätstests mit Abbildern virtueller Computer</span><span class="sxs-lookup"><span data-stu-id="fefb6-120">Application Compatibility Testing Using Virtual PC Images</span></span>](application-compatibility-testing-using-virtual-pc-images.md) | <span data-ttu-id="fefb6-121">Virtuelle PC-Images, die Kompatibilitätstests vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="fefb6-121">Virtual PC images that simplify compatibility testing.</span></span>                                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="fefb6-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fefb6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fefb6-123">Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="fefb6-123">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
