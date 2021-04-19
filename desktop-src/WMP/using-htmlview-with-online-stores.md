---
title: Verwenden von HtmlView mit Online Stores
description: Verwenden von HtmlView mit Online Stores
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player Online Stores, HtmlView
- Online Stores, HtmlView
- Typ 1 Online Stores, HtmlView
- Typ 2 Online Stores, HtmlView
- HtmlView, Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341479"
---
# <a name="using-htmlview-with-online-stores"></a><span data-ttu-id="fd15f-108">Verwenden von HtmlView mit Online Stores</span><span class="sxs-lookup"><span data-stu-id="fd15f-108">Using HTMLView with Online Stores</span></span>

<span data-ttu-id="fd15f-109">In Windows Media Player werden Benutzer aufgefordert, die Berechtigung zum Anzeigen von HtmlView-Inhalt in **jetzt Wiedergabe** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fd15f-109">Windows Media Player prompts users for permission to display HTMLView content in **Now Playing**.</span></span> <span data-ttu-id="fd15f-110">Online Stores können diese Eingabeaufforderung deaktivieren, indem Sie im **HtmlView** -Element des serviceInfo-Dokuments einen Basis-URL-Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="fd15f-110">Online stores can disable this prompt by specifying a base URL value in the **HTMLView** element of the ServiceInfo document.</span></span> <span data-ttu-id="fd15f-111">Wenn Windows Media Player eine Wiedergabeliste öffnet, die den zu Anzeige enden HtmlView-Inhalt angibt, vergleicht der Player die Basis-URL des serviceInfo-Dokuments des aktuellen aktiven Online Stores mit der Basis-URL des HtmlView-Inhalts.</span><span class="sxs-lookup"><span data-stu-id="fd15f-111">When Windows Media Player opens a playlist that specifies HTMLView content to display, the Player compares the base URL from the ServiceInfo document of the current active online store to the base URL of the HTMLView content.</span></span> <span data-ttu-id="fd15f-112">Wenn diese Stimmen, zeigt Windows Media Player den HtmlView-Inhalt an, ohne den Benutzer aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="fd15f-112">If they match, Windows Media Player displays the HTMLView content without prompting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd15f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd15f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd15f-114">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="fd15f-114">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="fd15f-115">**HtmlView-Element**</span><span class="sxs-lookup"><span data-stu-id="fd15f-115">**HTMLView Element**</span></span>](htmlview-element.md)
</dt> <dt>

[<span data-ttu-id="fd15f-116">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="fd15f-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




