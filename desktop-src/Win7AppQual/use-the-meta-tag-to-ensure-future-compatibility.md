---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Verwenden des Meta-Tags zum Sicherstellen der zukünftigen Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359617"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="cbda2-103">Verwenden des Meta-Tags zum Sicherstellen der zukünftigen Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="cbda2-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="cbda2-104">Windows Internet Explorer 8 ermöglicht Ihnen, den Dokument Kompatibilitätsmodus zu steuern, damit Sie den Browser anweisen können, Webseiten auf die gleiche Weise wie ältere Browserversionen zu renderieren.</span><span class="sxs-lookup"><span data-stu-id="cbda2-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="cbda2-105">Sie können auch auswählen, wann die Webseite aktualisiert werden soll, während Sie weiterhin verwendbar ist und ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="cbda2-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="cbda2-106">Festlegen des Meta-Elements</span><span class="sxs-lookup"><span data-stu-id="cbda2-106">Setting the Meta Element</span></span>

<span data-ttu-id="cbda2-107">Das **Meta** -Element enthält ein **Inhalts** Attribut, mit dem Sie den Modus angeben können, in dem der Inhalt für die Webseite gerendert wird, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbda2-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="cbda2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cbda2-108">Value</span></span> | <span data-ttu-id="cbda2-109">Renderingmodus</span><span class="sxs-lookup"><span data-stu-id="cbda2-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="cbda2-110">IE = 9</span><span class="sxs-lookup"><span data-stu-id="cbda2-110">IE=9</span></span>  | <span data-ttu-id="cbda2-111">Verwenden des Standard-Renderingmodus von Windows Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="cbda2-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="cbda2-112">IE = 8</span><span class="sxs-lookup"><span data-stu-id="cbda2-112">IE=8</span></span>  | <span data-ttu-id="cbda2-113">Verwenden des Standard-Renderingmodus von Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="cbda2-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="cbda2-114">IE = 7</span><span class="sxs-lookup"><span data-stu-id="cbda2-114">IE=7</span></span>  | <span data-ttu-id="cbda2-115">Verwenden des Standard-Renderingmodus von Windows Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="cbda2-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="cbda2-116">IE=5</span><span class="sxs-lookup"><span data-stu-id="cbda2-116">IE=5</span></span>  | <span data-ttu-id="cbda2-117">Verwenden des Standard-Renderingmodus von Microsoft Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="cbda2-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="cbda2-118">Weitere Informationen zur Kompatibilität und zum X-UA-kompatiblen Header finden Sie unter [Definieren der Dokument Kompatibilität](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="cbda2-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="cbda2-119">Im folgenden Codebeispiel wird veranschaulicht, wie Sie erzwingen können, dass eine Webseite im Internet Explorer 8-Modus gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="cbda2-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


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



## <a name="using-an-http-header"></a><span data-ttu-id="cbda2-120">Verwenden eines HTTP-Headers</span><span class="sxs-lookup"><span data-stu-id="cbda2-120">Using an HTTP Header</span></span>

<span data-ttu-id="cbda2-121">Viele Websites enthalten Tausende (oder Zehntausende) individuelle Webseiten, sodass das Festlegen des **Meta** -Elements für jedes Dokument nicht praktikabel ist.</span><span class="sxs-lookup"><span data-stu-id="cbda2-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="cbda2-122">Wenn Sie das **Meta** -Element für alle Seiten oder eine Auflistung von Seiten festlegen möchten, die nach Ordner ausgewählt sind, können Sie stattdessen die Serverkonfiguration anpassen und die X-UA-kompatiblen Metadaten im- [http-Header](/previous-versions/cc817572(v=msdn.10))hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cbda2-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="cbda2-123">Für Websites, die unterschiedliche **metaelementwerte** für Seiten auf demselben Server benötigen, gibt es mehrere Tools, die automatisch das entsprechende **Meta** -Element generieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="cbda2-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="cbda2-124">Das Hilfsprogramm " [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) " von Aggiorno fügt z. b. das Feature "Kompatibilitäts Kennzeichen für Internet Explorer 8" ein und entfernt es, sodass Ihre Website bestimmte Kompatibilitäts Standards erfüllen kann.</span><span class="sxs-lookup"><span data-stu-id="cbda2-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbda2-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbda2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbda2-126">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="cbda2-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
