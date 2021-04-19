---
description: Die directxmath-Bibliothek basiert auf der XNA Math C++ SIMD Library Version 2. x. Hier wird beschrieben, wie sich directxmath von XNA Math unterscheidet und wie sich directxmath-Versionen unterscheiden.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Neuigkeiten (directxmath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345217"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="cdd50-104">Neuigkeiten (directxmath)</span><span class="sxs-lookup"><span data-stu-id="cdd50-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="cdd50-105">Die directxmath-Bibliothek basiert auf der [XNA Math C++ SIMD Library, Version 2,04](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="cdd50-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="cdd50-106">Hier wird beschrieben, wie sich directxmath von XNA Math unterscheidet und wie sich directxmath-Versionen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="cdd50-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="cdd50-107">Rlease-Verlauf</span><span class="sxs-lookup"><span data-stu-id="cdd50-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="cdd50-108">Directxmath-Unterschiede von XNA math</span><span class="sxs-lookup"><span data-stu-id="cdd50-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="cdd50-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cdd50-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="cdd50-110">Releaseverlauf</span><span class="sxs-lookup"><span data-stu-id="cdd50-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="cdd50-111">Windows 10 Mai 2020 Update SDK</span><span class="sxs-lookup"><span data-stu-id="cdd50-111">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="cdd50-112">Directxmath 3,14</span><span class="sxs-lookup"><span data-stu-id="cdd50-112">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-113">SDK für Windows 10-Update vom Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="cdd50-113">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="cdd50-114">Directxmath 3,13</span><span class="sxs-lookup"><span data-stu-id="cdd50-114">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-115">Windows 10 April 2018 Update SDK</span><span class="sxs-lookup"><span data-stu-id="cdd50-115">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="cdd50-116">Windows 10 Fall Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="cdd50-116">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="cdd50-117">Directxmath 3,11</span><span class="sxs-lookup"><span data-stu-id="cdd50-117">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-118">Windows 10 Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="cdd50-118">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="cdd50-119">Directxmath 3,10</span><span class="sxs-lookup"><span data-stu-id="cdd50-119">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-120">SDK für Windows 10 Anniversary</span><span class="sxs-lookup"><span data-stu-id="cdd50-120">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="cdd50-121">Directxmath 3,09</span><span class="sxs-lookup"><span data-stu-id="cdd50-121">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-122">Windows 10 SDK (November 2015)</span><span class="sxs-lookup"><span data-stu-id="cdd50-122">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="cdd50-123">Directxmath 3,08</span><span class="sxs-lookup"><span data-stu-id="cdd50-123">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-124">Windows SDK für Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="cdd50-124">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="cdd50-125">Directxmath 3,07</span><span class="sxs-lookup"><span data-stu-id="cdd50-125">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-126">Windows SDK für Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdd50-126">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="cdd50-127">Directxmath 3,06</span><span class="sxs-lookup"><span data-stu-id="cdd50-127">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="cdd50-128">Windows SDK für Windows 8</span><span class="sxs-lookup"><span data-stu-id="cdd50-128">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="cdd50-129">Directxmath 3,03</span><span class="sxs-lookup"><span data-stu-id="cdd50-129">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="cdd50-130">Weitere Informationen finden Sie unter [directxmath-Releases](https://github.com/Microsoft/DirectXMath/releases) .</span><span class="sxs-lookup"><span data-stu-id="cdd50-130">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="cdd50-131">Directxmath-Unterschiede von XNA math</span><span class="sxs-lookup"><span data-stu-id="cdd50-131">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="cdd50-132">Die directxmath-Bibliothek unterscheidet sich in erster Linie von der XNA-mathematischen Bibliothek:</span><span class="sxs-lookup"><span data-stu-id="cdd50-132">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="cdd50-133">Directxmath ist nur C++ (Namespaces, über Ladungen, neue Vorlagen usw.).</span><span class="sxs-lookup"><span data-stu-id="cdd50-133">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="cdd50-134">Erfordert die c++ 11-Standard Bibliotheks Unterstützung (d. h. stdint. h usw.).</span><span class="sxs-lookup"><span data-stu-id="cdd50-134">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="cdd50-135">Systeminterne Arm-Neon-Unterstützung für die Windows RT-Plattform.</span><span class="sxs-lookup"><span data-stu-id="cdd50-135">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="cdd50-136">Neue Farb Funktionalität (Farb Raum Konvertierungen, .net-Farb Konstanten).</span><span class="sxs-lookup"><span data-stu-id="cdd50-136">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="cdd50-137">Begrenzungs Volumetypen (eine Version von, die sich zuvor im xnacollision-Header im DirectX SDK-Konflikt Beispiel befunden hat).</span><span class="sxs-lookup"><span data-stu-id="cdd50-137">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="cdd50-138">Es ist keine Xbox 360-Version verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cdd50-138">No Xbox 360 version is available.</span></span> <span data-ttu-id="cdd50-139">Das Xbox 360-XDK sendet weiterhin xnamath v2. x; Entfernen von Xbox 360-spezifischen Datentypen und Funktionsvarianten.</span><span class="sxs-lookup"><span data-stu-id="cdd50-139">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="cdd50-140">Überarbeitete [**xmvector perstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) Funktionen für eine verbesserte Optimierung der systeminternen SSE-und Arm-Neon-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="cdd50-140">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="cdd50-141">Der [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) -Typ ist vollständig undurchsichtig.</span><span class="sxs-lookup"><span data-stu-id="cdd50-141">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="cdd50-142">Wenn Sie auf einzelne Elemente von **xmmatrix** zugreifen möchten, verwenden Sie andere Typen, z. b. [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="cdd50-142">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdd50-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cdd50-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdd50-144">Directxmath-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="cdd50-144">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="cdd50-145">Directxmath-Releases</span><span class="sxs-lookup"><span data-stu-id="cdd50-145">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
