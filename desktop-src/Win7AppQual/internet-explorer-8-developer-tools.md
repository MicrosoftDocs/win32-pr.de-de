---
description: Internet Explorer 8-Entwicklertools
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Internet Explorer 8-Entwicklertools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a4314d5d0392b9bc4933b945f7da32040e1570
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088208"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="6ff37-103">Internet Explorer 8-Entwicklertools</span><span class="sxs-lookup"><span data-stu-id="6ff37-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="6ff37-104">Windows Internet Explorer 8 enthält das feature Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="6ff37-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="6ff37-105">Mit diesem Feature können Sie Microsoft JScript schnell debuggen, ein Windows-Internet Explorer-spezifisches Verhalten untersuchen oder schnell einen Prototyp erstellen oder eine neue Entwurfslösung testen.</span><span class="sxs-lookup"><span data-stu-id="6ff37-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="6ff37-106">In den folgenden Abschnitten werden die wichtigen Merkmale der Entwicklertools in Internet Explorer 8 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ff37-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="6ff37-107">Integriert und einfach zu verwenden</span><span class="sxs-lookup"><span data-stu-id="6ff37-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="6ff37-108">Die Entwicklertools sind in jeder Installation von Internet Explorer 8 enthalten, sodass Sie Probleme auf jedem Computer debuggen können, auf dem Internet Explorer 8 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ff37-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="6ff37-109">Darüber hinaus werden die Tools nur geladen, wenn Sie sie benötigen, um die Auswirkungen auf die Leistung des Browsers einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="6ff37-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="6ff37-110">Mithilfe der Entwicklertools können Sie schnell nur den aktuellen Internet Explorer Prozess debuggen, anstatt alle Internet Explorer zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="6ff37-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="6ff37-111">Bereitstellen einer grafischen Benutzeroberfläche für die Plattform</span><span class="sxs-lookup"><span data-stu-id="6ff37-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="6ff37-112">Anstatt die Funktionsweise Ihrer Website umgekehrt zu gestalten oder Ihre Website so zu ändern, dass Debuginformationen ausgegeben werden, können Sie mit dem Entwicklertools Internet Explorer untersuchen, um ihre Darstellung Ihrer Website anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ff37-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="6ff37-113">Diese Ansicht reduziert die Zeit für das Debuggen dynamischer Websites, bei denen die Quelluntersuchung nicht sinnvoll ist, oder das Untersuchen eines Internet Explorer-spezifischen Verhaltens, bei dem ein generisches Erstellungstool nicht helfen kann.</span><span class="sxs-lookup"><span data-stu-id="6ff37-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="6ff37-114">Aktivieren von schnellen Experimenten</span><span class="sxs-lookup"><span data-stu-id="6ff37-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="6ff37-115">Wenn Sie in früheren Versionen von Internet Explorer einen neuen Entwurf erstellen oder Fixes testen, bearbeiten Sie wahrscheinlich Ihre Quelle, speichern sie, aktualisieren Ihre Seite im Browser und wiederholen sie.</span><span class="sxs-lookup"><span data-stu-id="6ff37-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="6ff37-116">Die Entwicklertools dieses Szenario optimieren, indem Sie Es Ihnen ermöglichen, Ihre Website im Browser zu bearbeiten und Änderungen sofort anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ff37-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="6ff37-117">Optimieren der Anwendungsleistung</span><span class="sxs-lookup"><span data-stu-id="6ff37-117">Optimize Application Performance</span></span>

<span data-ttu-id="6ff37-118">Um Leistungsprobleme zu identifizieren und zu beheben, iterieren Sie wahrscheinlich, indem Sie sich jeweils auf ein Szenario konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="6ff37-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="6ff37-119">Mithilfe des Skriptprofilors im Entwicklertools können Sie Statistiken erfassen, einschließlich der Ausführungszeit und der Anzahl der Aufrufe einer JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="6ff37-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="6ff37-120">Sie können diese Informationen verwenden, während Sie Ihre Anwendung testen und den Profilbericht verwenden, um Leistungsengpässe schnell zu identifizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="6ff37-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="6ff37-121">Drücken Sie F12, während Sie eine Webseite anzeigen, oder klicken Sie im Menü **Extras** auf **Entwicklertools,** um auf die Entwicklertools zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6ff37-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ff37-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ff37-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ff37-123">Tools zum Debuggen von Webanwendungen und Add-Ons</span><span class="sxs-lookup"><span data-stu-id="6ff37-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



