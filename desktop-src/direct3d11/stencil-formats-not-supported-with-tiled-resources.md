---
title: Bei gekachelten Ressourcen werden keine Schablonen Formate unterstützt.
description: Formate mit Schablonen werden bei gekachelten Ressourcen nicht unterstützt.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036241"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a><span data-ttu-id="61b6a-103">Bei gekachelten Ressourcen werden keine Schablonen Formate unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61b6a-103">Stencil formats not supported with tiled resources</span></span>

<span data-ttu-id="61b6a-104">Formate mit Schablonen werden bei gekachelten Ressourcen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61b6a-104">Formats that contain stencil aren't supported with tiled resources.</span></span>

<span data-ttu-id="61b6a-105">Zu den Formaten, die die Schablone enthalten, gehören DXGI \_ \_ -Format D24 \_ unorm \_ S8 \_ uint (und Verwandte Formate in der R24G8-Familie) und DXGI- \_ Format \_ d32 \_ float \_ S8X24 \_ uint (und Verwandte Formate in der R32G8X24-Familie).</span><span class="sxs-lookup"><span data-stu-id="61b6a-105">Formats that contain stencil include DXGI\_FORMAT\_D24\_UNORM\_S8\_UINT (and related formats in the R24G8 family) and DXGI\_FORMAT\_D32\_FLOAT\_S8X24\_UINT (and related formats in the R32G8X24 family).</span></span>

<span data-ttu-id="61b6a-106">Einige Implementierungen speichern Tiefe und Schablone in separaten Zuordnungen, während andere diese in anderen speichern.</span><span class="sxs-lookup"><span data-stu-id="61b6a-106">Some implementations store depth and stencil in separate allocations while others store them together.</span></span> <span data-ttu-id="61b6a-107">Die Kachel Verwaltung für die beiden Schemas müsste anders sein, und die Unterschiede können von keiner einzelnen API abstrahiert oder rationalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="61b6a-107">Tile management for the two schemes would have to be different, and no single API can abstract or rationalize the differences.</span></span> <span data-ttu-id="61b6a-108">Für zukünftige Hardware wird die Unterstützung unabhängiger tiefen und Schablonen Oberflächen empfohlen, die jeweils unabhängig voneinander nebeneinander angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="61b6a-108">We recommend for future hardware to support independent depth and stencil surfaces, each independently tiled.</span></span> <span data-ttu-id="61b6a-109">die 32-Bit-Tiefe hätte 128 x 128 Kacheln, und die 8-Bit-Schablone hätte 256 x 256 Kacheln.</span><span class="sxs-lookup"><span data-stu-id="61b6a-109">32 bit depth would have 128x128 tiles, and 8 bit stencil would have 256x256 tiles.</span></span> <span data-ttu-id="61b6a-110">Daher müssten Anwendungen mit einer Fehlausrichtung der Kachel Form zwischen Tiefe und Schablone Leben.</span><span class="sxs-lookup"><span data-stu-id="61b6a-110">Therefore, applications would have to live with tile shape misalignment between depth and stencil.</span></span> <span data-ttu-id="61b6a-111">Das gleiche Problem ist jedoch bereits mit verschiedenen renderzieloberflächen-Formaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="61b6a-111">But the same problem exists with different render target surface formats already.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61b6a-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61b6a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61b6a-113">Prozessübergreifende Ressourcen übergreifende und Geräte Freigabe</span><span class="sxs-lookup"><span data-stu-id="61b6a-113">Tiled resource cross process and device sharing</span></span>](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




