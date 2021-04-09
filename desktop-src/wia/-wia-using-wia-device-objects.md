---
description: Ein Abbild Erstellungs Gerät wird in Windows-Abbild Beschaffung (WIA) als hierarchische Struktur von WIA-Element Objekten (iwiaitem-Schnittstellen) dargestellt.
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Verwenden von WIA-Geräte Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129388"
---
# <a name="using-wia-device-objects"></a><span data-ttu-id="312a5-103">Verwenden von WIA-Geräte Objekten</span><span class="sxs-lookup"><span data-stu-id="312a5-103">Using WIA Device Objects</span></span>

<span data-ttu-id="312a5-104">Ein Abbild Erstellungs Gerät wird in Windows-Abbild Beschaffung (WIA) als hierarchische Struktur von WIA-Element Objekten ([**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstellen) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="312a5-104">An imaging device is represented in Windows Image Acquisition (WIA) as a hierarchical tree of WIA item objects ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces).</span></span> <span data-ttu-id="312a5-105">In der Regel stellt der Stamm dieser Elementstruktur das Gerät selbst dar, während die anderen Elemente in der Struktur Bilder, für eine Kamera oder Scanbereiche für einen Scanner darstellen.</span><span class="sxs-lookup"><span data-stu-id="312a5-105">Typically, the root of this item tree represents the device itself, while the other items on the tree represent images, for a camera, or scanning regions, for a scanner.</span></span>

<span data-ttu-id="312a5-106">Anwendungen verwenden den WIA-Geräte-Manager zum Erstellen und Aufzählen von WIA-Geräten.</span><span class="sxs-lookup"><span data-stu-id="312a5-106">Applications use the WIA device manager to create and enumerate WIA devices.</span></span> <span data-ttu-id="312a5-107">In den folgenden Abschnitten wird erläutert, wie WIA-Geräte erstellt und verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="312a5-107">The following sections explain how to create and use WIA devices:</span></span>

-   [<span data-ttu-id="312a5-108">Auswählen eines Geräts</span><span class="sxs-lookup"><span data-stu-id="312a5-108">Selecting a Device</span></span>](-wia-selecting-a-device.md)
-   [<span data-ttu-id="312a5-109">WIA-Kamerageräte</span><span class="sxs-lookup"><span data-stu-id="312a5-109">WIA Camera Devices</span></span>](-wia-wia-camera-devices.md)
-   [<span data-ttu-id="312a5-110">WIA-Scanner-Geräte</span><span class="sxs-lookup"><span data-stu-id="312a5-110">WIA Scanner Devices</span></span>](-wia-wia-scanner-devices.md)

 

 



