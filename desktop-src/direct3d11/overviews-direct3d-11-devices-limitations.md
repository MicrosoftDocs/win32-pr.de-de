---
title: Einschränkungen beim Erstellen von Warp-und Referenz Geräten
description: Zum Erstellen von Warp-und Referenz Geräten in Direct3D 10,1 und Direct3D 11,0 sind einige Einschränkungen vorhanden. Diese Einschränkungen werden in diesem Thema erläutert.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315195"
---
# <a name="limitations-creating-warp-and-reference-devices"></a><span data-ttu-id="e2c30-104">Einschränkungen beim Erstellen von Warp-und Referenz Geräten</span><span class="sxs-lookup"><span data-stu-id="e2c30-104">Limitations Creating WARP and Reference Devices</span></span>

<span data-ttu-id="e2c30-105">Zum Erstellen von Warp-und Referenz Geräten in Direct3D 10,1 und Direct3D 11,0 sind einige Einschränkungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e2c30-105">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="e2c30-106">Diese Einschränkungen werden in diesem Thema erläutert.</span><span class="sxs-lookup"><span data-stu-id="e2c30-106">This topic discusses those limitations.</span></span>

<span data-ttu-id="e2c30-107">Die \_ Treiber Typen "d3d10 Driver \_ Type Warp" und " \_ d3d10 \_ Driver \_ Type Reference" \_ werden auf der d3d10 \_ Feature \_ Level \_ 9 \_ 1 bis d3d10 \_ Feature \_ Level \_ 9 \_ 3 Feature Levels in Direct3D 10,1 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2c30-107">The D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE driver types are not supported on the D3D10\_FEATURE\_LEVEL\_9\_1 through D3D10\_FEATURE\_LEVEL\_9\_3 feature levels in Direct3D 10.1.</span></span> <span data-ttu-id="e2c30-108">Außerdem wird der D3D \_ Driver \_ Type \_ Warp Driver Type auf D3D \_ Feature \_ Level \_ 11 \_ 0 in Direct3D 11,0 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2c30-108">Additionally, the D3D\_DRIVER\_TYPE\_WARP driver type is not supported on D3D\_FEATURE\_LEVEL\_11\_0 in Direct3D 11.0.</span></span> <span data-ttu-id="e2c30-109">Das heißt, wenn Sie [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) zum Erstellen eines Direct3D 10,1-Geräts oder zum Erstellen von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) zum Erstellen eines Direct3D 11,0-Geräts aufruft, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einer dieser Funktionsebenen im-Befehl angeben, ist der-Befehl ungültig.</span><span class="sxs-lookup"><span data-stu-id="e2c30-109">That is, when you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device or when you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.0 device, if you specify a combination of one of these driver types with one of these feature levels in the call, the call is invalid.</span></span> <span data-ttu-id="e2c30-110">Für Warp-und Referenzgeräte sind nur die folgenden Kombinationen von featureebenen, Runtimes und Treiber Typen gültig:</span><span class="sxs-lookup"><span data-stu-id="e2c30-110">Only the following combinations of feature levels, runtimes, and driver types are valid for WARP and Reference devices:</span></span>

-   <span data-ttu-id="e2c30-111">D3D \_ Driver \_ Type \_ Warp on all Feature Levels in Direct3D 11,1 (in Windows 8 enthalten)</span><span class="sxs-lookup"><span data-stu-id="e2c30-111">D3D\_DRIVER\_TYPE\_WARP on all feature levels in Direct3D 11.1, which Windows 8 includes</span></span>

    <span data-ttu-id="e2c30-112">D3D \_ Driver \_ Type \_ Reference on all Feature Levels in Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="e2c30-112">D3D\_DRIVER\_TYPE\_REFERENCE on all feature levels in Direct3D 11.1</span></span>

    <span data-ttu-id="e2c30-113">Wenn Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) zum Erstellen eines Direct3D 11,1-Geräts aufzurufen, ist der-Befehl gültig, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einem dieser featureebenen angeben.</span><span class="sxs-lookup"><span data-stu-id="e2c30-113">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="e2c30-114">D3D \_ Driver \_ Type \_ Warp on D3D \_ Feature \_ Level \_ 9 \_ 1 bis D3D \_ Feature \_ Level \_ 10 \_ 1 Feature Levels in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e2c30-114">D3D\_DRIVER\_TYPE\_WARP on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="e2c30-115">D3D \_ Driver \_ Type \_ Reference on D3D \_ Feature \_ Level \_ 9 \_ 1 bis D3D \_ Feature \_ Level \_ 11 \_ 0 Feature Levels in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e2c30-115">D3D\_DRIVER\_TYPE\_REFERENCE on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_11\_0 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="e2c30-116">Wenn Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) zum Erstellen eines Direct3D 11-Geräts aufzurufen, ist der-Befehl gültig, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einem dieser featureebenen angeben.</span><span class="sxs-lookup"><span data-stu-id="e2c30-116">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="e2c30-117">D3d10 \_ Driver \_ Type \_ Warp and d3d10 \_ Driver \_ Type \_ Reference on d3d10 \_ Feature \_ Level \_ 10 \_ 0 through d3d10 \_ Feature \_ Level \_ 10 \_ 1 Feature Levels in Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="e2c30-117">D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE on D3D10\_FEATURE\_LEVEL\_10\_0 through D3D10\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 10.1</span></span>

    <span data-ttu-id="e2c30-118">Wenn Sie [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) zum Erstellen eines Direct3D 10,1-Geräts aufzurufen, ist der-Befehl gültig, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einem dieser featureebenen angeben.</span><span class="sxs-lookup"><span data-stu-id="e2c30-118">When you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2c30-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2c30-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2c30-120">Geräte</span><span class="sxs-lookup"><span data-stu-id="e2c30-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="e2c30-121">Einführung in Direct3D 11 auf downlevelhardware</span><span class="sxs-lookup"><span data-stu-id="e2c30-121">Introduction to Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[<span data-ttu-id="e2c30-122">Vorgehensweise: Erstellen eines Warp-Geräts</span><span class="sxs-lookup"><span data-stu-id="e2c30-122">How To: Create a WARP Device</span></span>](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[<span data-ttu-id="e2c30-123">Vorgehensweise: Erstellen eines Referenz Geräts</span><span class="sxs-lookup"><span data-stu-id="e2c30-123">How To: Create a Reference Device</span></span>](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[<span data-ttu-id="e2c30-124">**D3d10 \_ - \_ Treibertyp**</span><span class="sxs-lookup"><span data-stu-id="e2c30-124">**D3D10\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[<span data-ttu-id="e2c30-125">**D3d10- \_ Funktion \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="e2c30-125">**D3D10\_FEATURE\_LEVEL1**</span></span>](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[<span data-ttu-id="e2c30-126">**D3D \_ - \_ Treibertyp**</span><span class="sxs-lookup"><span data-stu-id="e2c30-126">**D3D\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[<span data-ttu-id="e2c30-127">**D3D \_ - \_ Featureebene**</span><span class="sxs-lookup"><span data-stu-id="e2c30-127">**D3D\_FEATURE\_LEVEL**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 