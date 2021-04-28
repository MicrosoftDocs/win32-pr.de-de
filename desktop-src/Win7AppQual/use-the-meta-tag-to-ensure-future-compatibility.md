---
description: Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a69180470c60dffc772f20fe6c515ba3803cbf2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084168"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="84539-103">Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="84539-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="84539-104">Mit Windows Internet Explorer 8 können Sie dokumentkompatibilitätsmodi steuern, sodass Sie den Browser anweisen können, Webseiten auf die gleiche Weise wie ältere Browserversionen zu rendern.</span><span class="sxs-lookup"><span data-stu-id="84539-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="84539-105">Sie können auch auswählen, wann die Webseite aktualisiert werden soll, während sie weiterhin verwendet werden kann und ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="84539-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="84539-106">Festlegen des Metaelements</span><span class="sxs-lookup"><span data-stu-id="84539-106">Setting the Meta Element</span></span>

<span data-ttu-id="84539-107">Das **Metaelement** enthält ein **Inhaltsattribut,** mit dem Sie den Modus angeben können, in dem Der Inhalt für die Webseite gerendert wird, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="84539-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="84539-108">Wert</span><span class="sxs-lookup"><span data-stu-id="84539-108">Value</span></span> | <span data-ttu-id="84539-109">Renderingmodus</span><span class="sxs-lookup"><span data-stu-id="84539-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="84539-110">IE=9</span><span class="sxs-lookup"><span data-stu-id="84539-110">IE=9</span></span>  | <span data-ttu-id="84539-111">Verwenden des Windows Internet Explorer 9-Standardrenderingmodus</span><span class="sxs-lookup"><span data-stu-id="84539-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="84539-112">IE=8</span><span class="sxs-lookup"><span data-stu-id="84539-112">IE=8</span></span>  | <span data-ttu-id="84539-113">Verwenden des Internet Explorer 8-Standardrenderingmodus</span><span class="sxs-lookup"><span data-stu-id="84539-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="84539-114">IE=7</span><span class="sxs-lookup"><span data-stu-id="84539-114">IE=7</span></span>  | <span data-ttu-id="84539-115">Verwenden des Windows Internet Explorer 7-Standardrenderingmodus</span><span class="sxs-lookup"><span data-stu-id="84539-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="84539-116">IE=5</span><span class="sxs-lookup"><span data-stu-id="84539-116">IE=5</span></span>  | <span data-ttu-id="84539-117">Verwenden des Microsoft Internet Explorer 5-Standardrenderingmodus</span><span class="sxs-lookup"><span data-stu-id="84539-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="84539-118">Weitere Informationen zur Kompatibilität und zum X-UA-kompatiblen Header finden Sie unter [Definieren der Dokumentkompatibilität](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="84539-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="84539-119">Im folgenden Codebeispiel wird veranschaulicht, wie sie erzwingen, dass eine Webseite im 8 Internet Explorer gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="84539-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a><span data-ttu-id="84539-120">Verwenden eines HTTP-Headers</span><span class="sxs-lookup"><span data-stu-id="84539-120">Using an HTTP Header</span></span>

<span data-ttu-id="84539-121">Viele Websites enthalten Tausende (oder Zehntausende) einzelner Webseiten, sodass das Festlegen des **Metaelements** für jedes Dokument unpraktisch ist.</span><span class="sxs-lookup"><span data-stu-id="84539-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="84539-122">Wenn Sie das  Metaelement für alle Seiten oder eine Sammlung von Seiten festlegen möchten, die nach Ordner ausgewählt sind, können Sie stattdessen die Serverkonfiguration anpassen und die X-UA-kompatiblen Metadaten im [HTTP-Header hinzufügen.](/previous-versions/cc817572(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="84539-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="84539-123">Für Websites, die unterschiedliche **Metaelementwerte** für Seiten auf demselben Server benötigen, gibt es mehrere Tools, die automatisch das entsprechende **Metaelement** für Sie generieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="84539-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="84539-124">Beispielsweise fügt das [Hilfsprogramm ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) von Alayrno das Feature Internet Explorer 8-Kompatibilitätstags ein und entfernt es und kann Ihre Website dabei unterstützen, bestimmte Kompatibilitätsstandards zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="84539-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84539-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84539-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84539-126">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="84539-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
