---
description: VMR-Unterstützung für die DirectX-Video Beschleunigung
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: VMR-Unterstützung für die DirectX-Video Beschleunigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753809"
---
# <a name="vmr-support-for-directx-video-acceleration"></a><span data-ttu-id="5c0d4-103">VMR-Unterstützung für die DirectX-Video Beschleunigung</span><span class="sxs-lookup"><span data-stu-id="5c0d4-103">VMR Support for DirectX Video Acceleration</span></span>

<span data-ttu-id="5c0d4-104">Die DirectX-Video Beschleunigung ist eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und eine entsprechende Gerätetreiber Schnittstelle (DDI) für die Hardwarebeschleunigung der Verarbeitung digitaler Video Decodierung mit Unterstützung von Alpha Blending für solche Zwecke wie die Unterstützung von DVD-Unterbildern.</span><span class="sxs-lookup"><span data-stu-id="5c0d4-104">DirectX Video Acceleration is an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="5c0d4-105">DirectX VA ist im Windows-DDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="5c0d4-105">DirectX VA is documented in the Windows DDK.</span></span> <span data-ttu-id="5c0d4-106">Die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -Schnittstelle, die den Benutzermodus-Zugriff auf die DirectX-VA-Funktionalität auf einem Hardware Gerät bietet, ist in diesem SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="5c0d4-106">The [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, which provides user mode access to DirectX VA functionality on a hardware device, is documented in this SDK.</span></span>

<span data-ttu-id="5c0d4-107">VMR unterstützt [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), und die Implementierung ist mit dem alten Überlagerungs-Mixer identisch, mit Ausnahme eines wichtigen Unterschieds.</span><span class="sxs-lookup"><span data-stu-id="5c0d4-107">The VMR supports [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), and its implementation is identical to the old Overlay Mixer except for one important difference.</span></span> <span data-ttu-id="5c0d4-108">Der Überlagerungs Mixer garantierte, dass die Ausgabe in eine Überlagerungs Oberfläche gerendert wird, während der VMR die Ausgabe zur weiteren Verarbeitung senden kann, z. b. ein 3D-Vorgang, oder die Ausgabe an eine Offscreen-Oberfläche senden kann, die dann auf die primäre Oberfläche geblittet wird.</span><span class="sxs-lookup"><span data-stu-id="5c0d4-108">The Overlay Mixer guaranteed that the output is rendered into an overlay surface, while the VMR can send the output for further processing, for example a 3D operation, or it might send the output to an offscreen surface which is then blitted to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c0d4-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c0d4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c0d4-110">Informationen zur DirectX-Video Beschleunigung</span><span class="sxs-lookup"><span data-stu-id="5c0d4-110">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



