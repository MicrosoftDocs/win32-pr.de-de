---
title: DRM-Versionen
description: DRM-Versionen
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media-Format-SDK, DRM-Versionen
- Digital Rights Management (DRM), Versionen
- DRM (Digital Rights Management), Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947573"
---
# <a name="drm-versions"></a><span data-ttu-id="622dd-106">DRM-Versionen</span><span class="sxs-lookup"><span data-stu-id="622dd-106">DRM Versions</span></span>

<span data-ttu-id="622dd-107">Es gibt mehrere Versionen von Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="622dd-107">There are several versions of Windows Media digital rights management (DRM).</span></span> <span data-ttu-id="622dd-108">DRM-Version 1 wird häufig von den anderen Versionen in dieser Dokumentation getrennt, da Sie mithilfe von Verfahren implementiert wird, die sich von den neueren Versionen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="622dd-108">DRM version 1 is often set apart from the other versions in this documentation, because it is implemented using techniques that are different from the later versions.</span></span> <span data-ttu-id="622dd-109">Die zweite Generation von Windows Media DRM heißt DRM-Version 7, da Sie als Teil des Windows Media-Formats 7 SDK eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="622dd-109">The second generation of Windows Media DRM is called DRM version 7 because it was introduced as part of the Windows Media Format 7 SDK.</span></span> <span data-ttu-id="622dd-110">Sie wird manchmal als DRM-Version 2 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="622dd-110">It is sometimes called DRM version 2.</span></span> <span data-ttu-id="622dd-111">Bei den neueren Versionen von Windows Media DRM, DRM Version 9 und den neuen Windows Media DRM 10 handelt es sich um Erweiterungen der DRM-Version 7, und die gleichen Prozeduren werden für die Implementierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="622dd-111">The later versions of Windows Media DRM, DRM version 9 and the new Windows Media DRM 10, are extensions of DRM version 7 and use the same procedures for implementation.</span></span> <span data-ttu-id="622dd-112">Alle Versionen von Windows Media DRM verwenden dieselben Verschlüsselungs Routinen. die Unterschiede zwischen den Versionen müssen mit Lizenz Features durchzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="622dd-112">All versions of Windows Media DRM use the same encryption routines; the differences between versions have to do with license features.</span></span>

<span data-ttu-id="622dd-113">Wenn Sie geschützte Dateien mithilfe der Objekte des Windows Media Format SDK erstellen, sollten Sie sowohl Version 1 als auch die aktuellste Version unterstützen.</span><span class="sxs-lookup"><span data-stu-id="622dd-113">When you create protected files by using the objects of the Windows Media Format SDK, you should support both version 1 and the most current version.</span></span> <span data-ttu-id="622dd-114">Dateien, die von DRM-Version 1 geschützt werden, unterscheiden sich von Dateien, die durch höhere Versionen geschützt sind, nur im Inhalt des Headers</span><span class="sxs-lookup"><span data-stu-id="622dd-114">Files protected by DRM version 1 differ from files protected by later versions only in the contents of the header.</span></span> <span data-ttu-id="622dd-115">Neuere Dateien, die die zusätzlichen Header Informationen enthalten, können weiterhin auf Clients verwendet werden, die nur Inhalt der Version 1 darstellen.</span><span class="sxs-lookup"><span data-stu-id="622dd-115">Newer files that contain the additional header information can still be used on clients that render only version 1 content.</span></span> <span data-ttu-id="622dd-116">Obwohl spätere Versionen von DRM ein höheres Maß an Sicherheit und zusätzliche Features bieten, gibt es immer noch viele Spieler, die nur Version 1 verwenden.</span><span class="sxs-lookup"><span data-stu-id="622dd-116">While later versions of DRM offer a higher level of security and additional features, there are still many players that use only version 1.</span></span>

<span data-ttu-id="622dd-117">Weitere Informationen zu DRM-Versionen finden Sie in der Dokumentation zum Windows Media Rights Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="622dd-117">For more information on DRM versions, see the Windows Media Rights Manager SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="622dd-118">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="622dd-118">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="622dd-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="622dd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="622dd-120">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="622dd-120">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="622dd-121">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="622dd-121">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




