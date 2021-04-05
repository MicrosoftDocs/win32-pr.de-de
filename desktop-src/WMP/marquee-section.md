---
title: Marquee-Abschnitt
description: Marquee-Abschnitt
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Windows Media Player Mobile Skins, marquees
- Skins, marquees
- Erstellen von Skins, Marquee section
- Schreiben von Code für Skins, Marquee (Abschnitt)
- marquees in Skins, Marquee (Abschnitt)
- Skin-Definitions Dateien, Marquee-Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714519"
---
# <a name="marquee-section"></a><span data-ttu-id="3f38f-109">Marquee-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3f38f-109">Marquee Section</span></span>

<span data-ttu-id="3f38f-110">Der Marquee-Abschnitt enthält Informationen zum Marquee-Textfeld, in dem Scrolltext angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="3f38f-110">The Marquee section contains information about the marquee text box, which will display scrolling text:</span></span>


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



<span data-ttu-id="3f38f-111">Dadurch werden der Titel und der Autor des aktuellen Medien Elements angezeigt, obwohl Sie beliebige Texttypen im Marquee anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="3f38f-111">This will display the title and author of the current media item although you can display any text type in the marquee.</span></span> <span data-ttu-id="3f38f-112">Beispielsweise können Sie auch filename, Status und Wiedergabeliste in Ihrem Marquee einschließen.</span><span class="sxs-lookup"><span data-stu-id="3f38f-112">For example, you could also include Filename, Status, and Playlist in your marquee.</span></span>

> [!Note]  
> <span data-ttu-id="3f38f-113">Um die Kompatibilität mit Versionen von Windows Media Player Mobile zu gewährleisten, die älter als Windows Media Player 10 Mobile sind, wird die Verwendung von "Marquis" in einer Skin-Definitionsdatei weiterhin als gültig betrachtet.</span><span class="sxs-lookup"><span data-stu-id="3f38f-113">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="3f38f-114">Weitere Informationen zum Abschnitt "Marquee" finden Sie unter [Marquee](marquee.md) in der Skin-Referenz.</span><span class="sxs-lookup"><span data-stu-id="3f38f-114">For more about the Marquee section, see [Marquee](marquee.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f38f-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f38f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f38f-116">**Schreiben des Codes**</span><span class="sxs-lookup"><span data-stu-id="3f38f-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




