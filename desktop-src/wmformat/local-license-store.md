---
title: Lokaler Lizenz Speicher
description: Lokaler Lizenz Speicher
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), geschützte Datei Lizenzierung
- DRM (Digital Rights Management), geschützte Datei Lizenzierung
- Lizenzen, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388739"
---
# <a name="local-license-store"></a><span data-ttu-id="3c8ff-111">Lokaler Lizenz Speicher</span><span class="sxs-lookup"><span data-stu-id="3c8ff-111">Local License Store</span></span>

<span data-ttu-id="3c8ff-112">Wenn eine DRM-Lizenz an den Client Computer übermittelt wird, wird Sie im lokalen Lizenz Speicher abgelegt.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-112">When a DRM license is delivered to the client computer it is put into the local license store.</span></span> <span data-ttu-id="3c8ff-113">Dabei handelt es sich um eine geschützte Datei auf der Festplatte, die alle für den Benutzer ausgegebenen Lizenzen sowie andere DRM-Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-113">This is a protected file on the hard disk that contains all the licenses issued to the user along with other DRM information.</span></span>

<span data-ttu-id="3c8ff-114">Sie können Daten im lokalen Lizenz Speicher auf einige beschränkte Weise mithilfe der erweiterten APIs des Windows Media DRM-Clients bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-114">You can manipulate data in the local license store in a few, limited ways by using the Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="3c8ff-115">Zusätzlich zum lokalen Lizenz Speicher verwenden einige Objekte einen temporären Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-115">In addition to the local license store, some objects make use of a temporary license store.</span></span> <span data-ttu-id="3c8ff-116">Eine Lizenz in einem temporären Speicher ist nur für kurze Zeit vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-116">A license in a temporary store exists only for a short period of time.</span></span> <span data-ttu-id="3c8ff-117">Allerdings können einige Lizenzen, die in einem temporären Speicher beginnen, im regulären lokalen Lizenz Speicher gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3c8ff-117">However, some licenses that begin in a temporary store can be saved to the regular local license store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c8ff-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c8ff-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c8ff-119">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="3c8ff-119">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




