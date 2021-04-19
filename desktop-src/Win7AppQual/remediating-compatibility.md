---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: DEP/NX-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364287"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="77bdc-103">DEP/NX-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="77bdc-103">DEP/NX compatibility</span></span>

<span data-ttu-id="77bdc-104">In Windows Internet Explorer 7 wird DEP/NX standardmäßig aus Kompatibilitätsgründen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="77bdc-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="77bdc-105">Mehrere beliebte Add-ons sind nicht mit DEP/NX kompatibel und schlagen fehl, wenn Sie von Windows Internet Explorer mit aktiviertem DEP/NX geladen werden.</span><span class="sxs-lookup"><span data-stu-id="77bdc-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="77bdc-106">In der Regel werden diese Add-ons mithilfe einer älteren Version des ATL-Frameworks erstellt.</span><span class="sxs-lookup"><span data-stu-id="77bdc-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="77bdc-107">ATL 7,1 und frühere Versionen sind nicht mit dem DEP-Sicherheits Feature konzipiert.</span><span class="sxs-lookup"><span data-stu-id="77bdc-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="77bdc-108">Glücklicherweise verfügen neue Versionen von Microsoft Windows Service Packs über neue DEP/NX-APIs, die es Ihnen ermöglichen, DEP/NX zu verwenden und die Kompatibilität mit älteren ATL-Versionen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="77bdc-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="77bdc-109">Diese neuen APIs ermöglichen es Internet Explorer, DEP/NX zu abonnieren, ohne dass Add-ons, die mit älteren Versionen von ATL erstellt wurden, fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="77bdc-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="77bdc-110">Wenn ein Add-on nicht mit DEP/NX kompatibel ist und keinen veralteten ATL-Code verwendet, können Sie eine Gruppenrichtlinie Option verwenden, um DEP/NX für Internet Explorer zu abonnieren, bis eine aktualisierte Version des unterbrochenen Steuer Elements bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="77bdc-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="77bdc-111">Lokale Administratoren können DEP/NX steuern, indem Sie Internet Explorer als Administrator ausführen und die Option **Speicherschutz aktivieren** im **erweiterten** Bereich der **Internet Optionen** löschen.</span><span class="sxs-lookup"><span data-stu-id="77bdc-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77bdc-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77bdc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77bdc-113">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="77bdc-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
