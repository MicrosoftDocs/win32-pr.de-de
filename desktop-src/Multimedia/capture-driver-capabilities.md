---
title: Erfassungs Treiberfunktionen
description: Erfassungs Treiberfunktionen
ms.assetid: 6e74635e-9dac-419d-a264-08fee04ae7b7
keywords:
- WM_CAP_DRIVER_GET_CAPS Meldung
- capdrivergetcaps-Makro
- Capdrivercaps-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87fb4f9cb439229721b6c10aa6207af601f9ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036562"
---
# <a name="capture-driver-capabilities"></a><span data-ttu-id="9fec6-106">Erfassungs Treiberfunktionen</span><span class="sxs-lookup"><span data-stu-id="9fec6-106">Capture Driver Capabilities</span></span>

<span data-ttu-id="9fec6-107">Sie können die Hardwarefunktionen des derzeit verbundenen Erfassungs Treibers mithilfe der Nachricht " [**WM- \_ Cap- \_ Treiber \_ get \_ Caps**](wm-cap-driver-get-caps.md) " (oder dem " [**capdrivergetcaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) "-Makro) abrufen.</span><span class="sxs-lookup"><span data-stu-id="9fec6-107">You can retrieve the hardware capabilities of the currently connected capture driver by using the [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message (or the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro).</span></span> <span data-ttu-id="9fec6-108">Diese Meldung gibt die Funktionen des Aufzeichnungs Treibers und der zugrunde liegenden Hardware in der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="9fec6-108">This message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

 

 




