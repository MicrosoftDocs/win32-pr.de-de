---
title: Informationen zum DVD-Objekt
description: Informationen zum DVD-Objekt
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player, DVD-Objekt
- Windows Media Player-Objektmodell, DVD-Objekt
- Objektmodell, DVD-Objekt
- Windows Media Player ActiveX-Steuerelement, DVD-Objekt
- ActiveX-Steuerelement, DVD-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, DVD-Objekt
- Windows Media Player Mobile, DVD-Objekt
- DVD-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309303"
---
# <a name="about-the-dvd-object"></a><span data-ttu-id="8fd2e-111">Informationen zum DVD-Objekt</span><span class="sxs-lookup"><span data-stu-id="8fd2e-111">About the DVD Object</span></span>

<span data-ttu-id="8fd2e-112">Das **DVD** -Objekt fügt für DVD-medienspezifische Funktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="8fd2e-112">The **DVD** object adds functionality specific to DVD media.</span></span> <span data-ttu-id="8fd2e-113">Im Allgemeinen werden DVD-Medien wie andere digitale Medien in Windows Media Player behandelt.</span><span class="sxs-lookup"><span data-stu-id="8fd2e-113">In a general sense, DVD media is treated just like other digital media in Windows Media Player.</span></span> <span data-ttu-id="8fd2e-114">Beispielsweise werden DVD-Laufwerke mithilfe des **cdromcollection** -Objekts aufgelistet, und DVD-Titel und-Kapitel werden mithilfe von **Wiedergabe** Listen Objekten und **Medien** Objekten manipuliert.</span><span class="sxs-lookup"><span data-stu-id="8fd2e-114">For instance, DVD drives are enumerated using the **CdromCollection** object and DVD titles and chapters are manipulated using **Playlist** objects and **Media** objects.</span></span> <span data-ttu-id="8fd2e-115">Einige Funktionen sind jedoch DVD-spezifisch, und das **DVD** -Objekt stellt dies bereit.</span><span class="sxs-lookup"><span data-stu-id="8fd2e-115">Some functionality is DVD-specific, however, and the **DVD** object provides this.</span></span> <span data-ttu-id="8fd2e-116">Beispielsweise hat die DVD ein Konzept namens "Domäne".</span><span class="sxs-lookup"><span data-stu-id="8fd2e-116">For example, DVD has a concept called domain.</span></span> <span data-ttu-id="8fd2e-117">Zum Abrufen der aktuellen Domäne für DVD-Medien geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="8fd2e-117">To retrieve the current domain for DVD media, type the following:</span></span>


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a><span data-ttu-id="8fd2e-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8fd2e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fd2e-119">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="8fd2e-119">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="8fd2e-120">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="8fd2e-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




