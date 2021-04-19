---
description: Per-Pixel Alpha Blending
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel Alpha Blending
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346598"
---
# <a name="per-pixel-alpha-blending"></a><span data-ttu-id="2b3e0-103">Per-Pixel Alpha Blending</span><span class="sxs-lookup"><span data-stu-id="2b3e0-103">Per-Pixel Alpha Blending</span></span>

<span data-ttu-id="2b3e0-104">Es wurden vier Medien Untertypen für die Alpha Mischung pro Pixel definiert.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-104">Four media subtypes have been defined for per-pixel alpha blending.</span></span> <span data-ttu-id="2b3e0-105">Diese Untertypen werden nur unterstützt, wenn sich der VMR im Mischungs Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-105">These subtypes are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="2b3e0-106">Die VMR lehnt die Verbindung ab, wenn Sie sich nicht im Mischungs Modus befindet, wenn ein upstreamfilter versucht, eine Verbindung mit einem dieser Untertypen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-106">The VMR will reject the connection if it is not in mixing mode when an upstream filter attempts to connect using one of these subtypes.</span></span> <span data-ttu-id="2b3e0-107">Diese Untertypen sind in UUIDs. h definiert:</span><span class="sxs-lookup"><span data-stu-id="2b3e0-107">These subtypes are defined in uuids.h:</span></span>

-   <span data-ttu-id="2b3e0-108">Mediasubtype \_ ARGB1555</span><span class="sxs-lookup"><span data-stu-id="2b3e0-108">MEDIASUBTYPE\_ARGB1555</span></span>
-   <span data-ttu-id="2b3e0-109">Mediasubtype \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="2b3e0-109">MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="2b3e0-110">Mediasubtype \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="2b3e0-110">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="2b3e0-111">mediasubtype \_ ayuv</span><span class="sxs-lookup"><span data-stu-id="2b3e0-111">MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="2b3e0-112">Weitere Informationen finden Sie unter [unkomprimierte RGB-Video Untertypen](uncompressed-rgb-video-subtypes.md) und [**YUV-Video Untertypen**](yuv-video-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-112">For more information, see [Uncompressed RGB Video Subtypes](uncompressed-rgb-video-subtypes.md) and [**YUV Video Subtypes**](yuv-video-subtypes.md).</span></span>

 

 



