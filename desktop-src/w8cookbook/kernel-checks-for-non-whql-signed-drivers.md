---
title: Kernel Überprüfungen für nicht-WHQL-signierte Treiber
description: Bei Geräten, die die Installation von Windows 10 bereinigen und bei denen der sichere Start auf ON fest steht (Beachten Sie, dass dies für alle neuen Geräte seit der Veröffentlichung von Windows 8,0 der Standard ist), müssen alle neuen Treiber von WHQL/sysdev signiert werden, anstatt nur Kreuz signierte Zertifikate zu verwenden.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388592"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a><span data-ttu-id="e2298-103">Kernel Überprüfungen für nicht-WHQL-signierte Treiber</span><span class="sxs-lookup"><span data-stu-id="e2298-103">Kernel checks for non-WHQL signed drivers</span></span>

<span data-ttu-id="e2298-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e2298-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e2298-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e2298-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e2298-106">Bei Geräten, die die Installation von Windows 10 bereinigen und bei denen der sichere Start auf ON fest steht (Beachten Sie, dass dies für alle neuen Geräte seit der Veröffentlichung von Windows 8,0 der Standard ist), müssen alle neuen Treiber von WHQL/sysdev signiert werden, anstatt nur Kreuz signierte Zertifikate zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2298-106">For devices that clean install Windows 10, and where Secure Boot is on (note that this is standard for all new devices since the release of Windows 8.0), all new drivers must be signed by WHQL/Sysdev rather than just use cross-signed certificates.</span></span> <span data-ttu-id="e2298-107">Geräte, für die ein Upgrade durchgeführt wurde, und Fälle, in denen Treiber mit einem Kreuz Zertifikat signiert wurden, bevor diese Richtlinie wirksam wird, werden von dieser Richtlinie ausgeschlossen, um die Abwärtskompatibilität sicherzustellen</span><span class="sxs-lookup"><span data-stu-id="e2298-107">Devices that are upgraded and cases where drivers have been signed with a cross-cert before this policy went into effect are excluded from this policy to ensure backwards compatibility.</span></span> <span data-ttu-id="e2298-108">Diese Richtlinie wurde am 2015. April angekündigt, Sie wird jedoch mit der Windows Anniversary Edition (Version August 2016) erzwungen.</span><span class="sxs-lookup"><span data-stu-id="e2298-108">This policy was announced April 2015, however it will be enforced with the Windows Anniversary Edition, released August 2016.</span></span>

<span data-ttu-id="e2298-109">In Fällen, in denen ein Treiber nicht ordnungsgemäß signiert ist, wird er als PCA-Benachrichtigung angezeigt, dass die Treiber blockiert werden, wenn Sie die Signatur Anforderungen nicht bestehen.</span><span class="sxs-lookup"><span data-stu-id="e2298-109">In cases where a driver is not signed correctly, it will manifest as a PCA notification that the driver(s) is blocked when it doesn’t pass signature requirements.</span></span> <span data-ttu-id="e2298-110">Dadurch wird verhindert, dass der Treiber, der nicht mehr im Kernel blockiert wird, transparent blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="e2298-110">This prevents a later disconnected user experience of the driver being blocked in kernel transparently.</span></span>

<span data-ttu-id="e2298-111">Weitere Informationen finden Sie in [diesem Blogbeitrag](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), in dem die Treiber Signier Änderung angekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2298-111">For more information, please refer to [this blog post](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), which announces the driver signing change.</span></span>

 

 




