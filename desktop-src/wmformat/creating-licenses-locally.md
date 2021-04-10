---
title: Lokales Erstellen von Lizenzen
description: Lokales Erstellen von Lizenzen
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows Media-Format-SDK, lokales Erstellen von Lizenzen
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), lokales Erstellen von Lizenzen
- DRM (Digital Rights Management), lokales Erstellen von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, lokale Lizenzen erstellen
- Erweiterte Client-APIs, Erstellen von Lizenzen lokal
- Lizenzen, lokales Erstellen von Lizenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037581"
---
# <a name="creating-licenses-locally"></a><span data-ttu-id="679de-112">Lokales Erstellen von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="679de-112">Creating Licenses Locally</span></span>

<span data-ttu-id="679de-113">Unter bestimmten Umständen, z. b. beim [DRM-Import](drm-import.md), können Sie Ihre eigenen Lizenzen erstellen.</span><span class="sxs-lookup"><span data-stu-id="679de-113">In certain circumstances, such as during [DRM Import](drm-import.md), you can create your own licenses.</span></span> <span data-ttu-id="679de-114">Windows Media DRM-Lizenzen können auf verschiedene Arten geschrieben werden, aber um Ihre eigene Lizenz zu erstellen, müssen Sie das binäre XMR-Schema (Extensible Media Rights) verwenden.</span><span class="sxs-lookup"><span data-stu-id="679de-114">Windows Media DRM licenses can be written a few different ways, but to make your own license, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="679de-115">Weitere Informationen finden Sie unter [Building a XMR License](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="679de-115">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>

<span data-ttu-id="679de-116">Wenn Sie eine Lizenz erstellen, können Sie Sie dem lokalen Lizenz Speicher hinzufügen, indem Sie die [**iwmdrmlicensetmanagement:: storelicense**](iwmdrmlicensemanagement-storelicense.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="679de-116">When you create a license, you can add it to the local license store by calling the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="679de-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="679de-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="679de-118">**Erwerben von Lizenzen**</span><span class="sxs-lookup"><span data-stu-id="679de-118">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="679de-119">**Aufbauen einer XMR-Lizenz**</span><span class="sxs-lookup"><span data-stu-id="679de-119">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> </dl>

 

 




