---
title: Verweisen auf Skins in URLs
description: Verweisen auf Skins in URLs
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Windows Media Player Skins, URL-Verweise
- Skins, URL-Verweise
- URL-Verweise in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714046"
---
# <a name="referencing-skins-in-urls"></a><span data-ttu-id="9f81a-106">Verweisen auf Skins in URLs</span><span class="sxs-lookup"><span data-stu-id="9f81a-106">Referencing Skins in URLs</span></span>

<span data-ttu-id="9f81a-107">Wenn Sie eine-URL zum Laden einer Mediendatei verwenden, die von Windows Media Player abgespielt wird, können Sie anfordern, dass eine bestimmte Skin mit dieser Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f81a-107">If you use a URL to load a media file that will be played by Windows Media Player, you can request that a particular skin be used with that file.</span></span> <span data-ttu-id="9f81a-108">Wenn das Skin bereits auf dem Computer des Benutzers installiert ist, wird es verwendet. Andernfalls wird das vorherige Skin verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f81a-108">If the skin is already installed on the user's machine, it will be used; otherwise the previous skin will be used.</span></span>

<span data-ttu-id="9f81a-109">Fügen Sie am Ende der URL Folgendes ein, um eine Skin anzufordern:</span><span class="sxs-lookup"><span data-stu-id="9f81a-109">To request a skin, add the following to the end of the URL:</span></span>


```C++
?WMPSkin=skinname
```



<span data-ttu-id="9f81a-110">" *Skinname* " ist der Name der Skin, die Sie anfordern möchten.</span><span class="sxs-lookup"><span data-stu-id="9f81a-110">*skinname* is the name of the skin you want to request.</span></span> <span data-ttu-id="9f81a-111">Verwenden Sie keine Anführungszeichen um den Namen der Skin.</span><span class="sxs-lookup"><span data-stu-id="9f81a-111">Do not use quotes around the name of the skin.</span></span>

<span data-ttu-id="9f81a-112">Geben Sie z. b. die folgende http-URL ein, um die Verwendung von Headspace Skin anzufordern:</span><span class="sxs-lookup"><span data-stu-id="9f81a-112">For example, to request the headspace skin be used, type the following http URL:</span></span>


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a><span data-ttu-id="9f81a-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f81a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f81a-114">**Informationen zu Skins**</span><span class="sxs-lookup"><span data-stu-id="9f81a-114">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




