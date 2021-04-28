---
description: DEP/NX-Kompatibilität
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: DEP/NX-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116428"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="28a1f-103">DEP/NX-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="28a1f-103">DEP/NX compatibility</span></span>

<span data-ttu-id="28a1f-104">In Windows Internet Explorer 7 ist DEP/NX aus Kompatibilitätsgründen standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="28a1f-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="28a1f-105">Mehrere beliebte Add-Ons sind nicht mit DEP/NX kompatibel und schlagen fehl, wenn Windows Internet Explorer sie mit aktivierter DEP/NX lädt.</span><span class="sxs-lookup"><span data-stu-id="28a1f-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="28a1f-106">In der Regel werden diese Add-Ons mit einer älteren Version des ATL-Frameworks erstellt.</span><span class="sxs-lookup"><span data-stu-id="28a1f-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="28a1f-107">ATL 7.1 und frühere Versionen sind nicht mit dem DEP-Sicherheitsfeature konzipiert.</span><span class="sxs-lookup"><span data-stu-id="28a1f-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="28a1f-108">Glücklicherweise verfügen neue Versionen von Microsoft Windows Service Packs über neue DEP-/NX-APIs, mit denen Sie DEP/NX verwenden und die Kompatibilität mit älteren ATL-Versionen beibehalten können.</span><span class="sxs-lookup"><span data-stu-id="28a1f-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="28a1f-109">Diese neuen APIs ermöglichen es Internet Explorer, SICH für DEP/NX zu entscheiden, ohne dass Add-Ons, die mit älteren AtL-Versionen erstellt wurden, fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="28a1f-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="28a1f-110">Wenn ein Add-On nicht DEP-/NX-kompatibel ist und keine veraltete ATL verwendet, können Sie eine Gruppenrichtlinie Option verwenden, um DEP/NX für Internet Explorer zu deaktivieren, bis eine aktualisierte Version des fehlerhaften Steuerelements bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="28a1f-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="28a1f-111">Lokale Administratoren können DEP/NX steuern, indem sie Internet Explorer als Administrator ausführen und die Option **Speicherschutz aktivieren** im Bereich **Erweitert** von **Internetoptionen** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="28a1f-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28a1f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28a1f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28a1f-113">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="28a1f-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
