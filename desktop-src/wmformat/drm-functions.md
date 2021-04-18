---
title: Microsoft Windows Media DRM-Client Funktionen
description: Microsoft Windows Media DRM-Client Funktionen
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media-Format-SDK, Funktionen
- Digital Rights Management (DRM), Funktionen
- DRM (Digital Rights Management), Funktionen
- Erweiterte APIs für den DRM-Client, Funktionen
- Erweiterte Client-APIs, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337697"
---
# <a name="microsoft-windows-media-drm-client-functions"></a><span data-ttu-id="2da8c-108">Microsoft Windows Media DRM-Client Funktionen</span><span class="sxs-lookup"><span data-stu-id="2da8c-108">Microsoft Windows Media DRM Client Functions</span></span>

<span data-ttu-id="2da8c-109">Die folgenden Funktionen werden als Teil der erweiterten APIs für den Microsoft Windows Media DRM-Client implementiert.</span><span class="sxs-lookup"><span data-stu-id="2da8c-109">The following functions are implemented as part of the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="2da8c-110">Funktion</span><span class="sxs-lookup"><span data-stu-id="2da8c-110">Function</span></span>                                                             | <span data-ttu-id="2da8c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2da8c-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2da8c-112">**Wmdrmkreateprovider**</span><span class="sxs-lookup"><span data-stu-id="2da8c-112">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)                   | <span data-ttu-id="2da8c-113">Erstellt eine Klassenfactory, mit der die anderen DRM-Objekte erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="2da8c-113">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="2da8c-114">Diese Funktion erfordert keine stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Funktionen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2da8c-114">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span> |
| [<span data-ttu-id="2da8c-115">**Wmdrmkreateprotectedprovider**</span><span class="sxs-lookup"><span data-stu-id="2da8c-115">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md) | <span data-ttu-id="2da8c-116">Erstellt eine Klassenfactory, mit der die anderen DRM-Objekte erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="2da8c-116">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="2da8c-117">Diese Funktion erfordert eine stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Features unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2da8c-117">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>                |
| [<span data-ttu-id="2da8c-118">**Wmdrmshutdown**</span><span class="sxs-lookup"><span data-stu-id="2da8c-118">**WMDRMShutdown**</span></span>](wmdrmshutdown.md)                               | <span data-ttu-id="2da8c-119">Gibt die von den APIs verwendeten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="2da8c-119">Releases resources used by the APIs.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="2da8c-120">**Wmdrmstartup**</span><span class="sxs-lookup"><span data-stu-id="2da8c-120">**WMDRMStartup**</span></span>](wmdrmstartup.md)                                 | <span data-ttu-id="2da8c-121">Initialisiert Ressourcen, die von den APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2da8c-121">Initializes resources used by the APIs.</span></span>                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="2da8c-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2da8c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da8c-123">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="2da8c-123">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




