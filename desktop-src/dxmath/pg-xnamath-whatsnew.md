---
description: Die DirectXMath-Bibliothek basiert auf der XNA Math C++-SIMD-Bibliotheksversion 2.x. Hier wird beschrieben, wie sich DirectXMath von XNA Math unterscheidet und wie sich DirectXMath-Versionen unterscheiden.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Neues (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827626"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="2eb81-104">Neues (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="2eb81-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="2eb81-105">Die DirectXMath-Bibliothek basiert auf der [XNA Math C++-SIMD-Bibliotheksversion 2.04.](https://walbourn.github.io/xna-math-version-2-04/)</span><span class="sxs-lookup"><span data-stu-id="2eb81-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span></span> <span data-ttu-id="2eb81-106">Hier wird beschrieben, wie sich DirectXMath von XNA Math unterscheidet und wie sich DirectXMath-Versionen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2eb81-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="2eb81-107">Rlease-Verlauf</span><span class="sxs-lookup"><span data-stu-id="2eb81-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="2eb81-108">DirectXMath-Unterschiede zu XNA Math</span><span class="sxs-lookup"><span data-stu-id="2eb81-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="2eb81-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2eb81-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="2eb81-110">Releaseverlauf</span><span class="sxs-lookup"><span data-stu-id="2eb81-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="2eb81-111">Windows 10 SDK (20348), Version 2104</span><span class="sxs-lookup"><span data-stu-id="2eb81-111">Windows 10 SDK (20348), version 2104</span></span></td><td><span data-ttu-id="2eb81-112">DirectXMath 3.16</span><span class="sxs-lookup"><span data-stu-id="2eb81-112">DirectXMath 3.16</span></span></td>
 </td>
 <tr>
  <td><span data-ttu-id="2eb81-113">Windows 10 Update SDK von Mai 2020</span><span class="sxs-lookup"><span data-stu-id="2eb81-113">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="2eb81-114">DirectXMath 3.14</span><span class="sxs-lookup"><span data-stu-id="2eb81-114">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-115">Windows 10 October 2018 Update SDK</span><span class="sxs-lookup"><span data-stu-id="2eb81-115">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="2eb81-116">DirectXMath 3.13</span><span class="sxs-lookup"><span data-stu-id="2eb81-116">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-117">Windows 10 April 2018 Update SDK</span><span class="sxs-lookup"><span data-stu-id="2eb81-117">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="2eb81-118">Windows 10 Fall Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="2eb81-118">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="2eb81-119">DirectXMath 3.11</span><span class="sxs-lookup"><span data-stu-id="2eb81-119">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-120">Windows 10 Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="2eb81-120">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="2eb81-121">DirectXMath 3.10</span><span class="sxs-lookup"><span data-stu-id="2eb81-121">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-122">SDK für Windows 10 Anniversary</span><span class="sxs-lookup"><span data-stu-id="2eb81-122">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="2eb81-123">DirectXMath 3.09</span><span class="sxs-lookup"><span data-stu-id="2eb81-123">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-124">Windows 10 SDK (November 2015)</span><span class="sxs-lookup"><span data-stu-id="2eb81-124">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="2eb81-125">DirectXMath 3.08</span><span class="sxs-lookup"><span data-stu-id="2eb81-125">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-126">Windows SDK für Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="2eb81-126">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="2eb81-127">DirectXMath 3.07</span><span class="sxs-lookup"><span data-stu-id="2eb81-127">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-128">Windows SDK für Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2eb81-128">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="2eb81-129">DirectXMath 3.06</span><span class="sxs-lookup"><span data-stu-id="2eb81-129">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="2eb81-130">Windows SDK für Windows 8</span><span class="sxs-lookup"><span data-stu-id="2eb81-130">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="2eb81-131">DirectXMath 3.03</span><span class="sxs-lookup"><span data-stu-id="2eb81-131">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="2eb81-132">Weitere [Informationen finden Sie unter DirectXMath-Releases.](https://github.com/Microsoft/DirectXMath/releases)</span><span class="sxs-lookup"><span data-stu-id="2eb81-132">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="2eb81-133">DirectXMath-Unterschiede zu XNA Math</span><span class="sxs-lookup"><span data-stu-id="2eb81-133">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="2eb81-134">Die DirectXMath-Bibliothek unterscheidet sich in erster Linie von der XNA Math-Bibliothek:</span><span class="sxs-lookup"><span data-stu-id="2eb81-134">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="2eb81-135">DirectXMath ist nur C++ (Namespaces, Überladungen, neue Vorlagen und so weiter).</span><span class="sxs-lookup"><span data-stu-id="2eb81-135">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="2eb81-136">Erfordert C++11-Standardbibliotheksunterstützung (d. h. stdint.h und so weiter).</span><span class="sxs-lookup"><span data-stu-id="2eb81-136">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="2eb81-137">Systeminterne ARM-NEON-Unterstützung für die Windows RT Plattform.</span><span class="sxs-lookup"><span data-stu-id="2eb81-137">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="2eb81-138">Neue Farbfunktionalität (Farbraumkonvertierungen, .NET-Farbkonst constants).</span><span class="sxs-lookup"><span data-stu-id="2eb81-138">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="2eb81-139">Begrenzungsvolumentypen (eine Version von , die zuvor im XNACollision-Header im DirectX SDK Collision-Beispiel enthalten war).</span><span class="sxs-lookup"><span data-stu-id="2eb81-139">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="2eb81-140">Es Xbox 360 Version nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2eb81-140">No Xbox 360 version is available.</span></span> <span data-ttu-id="2eb81-141">Das Xbox 360 XDK wird weiterhin XNAMath v2.x liefern. Entfernen von Xbox 360 Datentypen und Funktionsvarianten.</span><span class="sxs-lookup"><span data-stu-id="2eb81-141">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="2eb81-142">Überarbeitete [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) für verbesserte Optimierung für systeminterne SSE- und ARM-NEON-Systema.</span><span class="sxs-lookup"><span data-stu-id="2eb81-142">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="2eb81-143">Der [**XMMATRIX-Typ**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) ist vollständig deckend.</span><span class="sxs-lookup"><span data-stu-id="2eb81-143">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="2eb81-144">Um auf einzelne Elemente von **XMMATRIX** zu zugreifen, verwenden Sie andere Typen wie [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="2eb81-144">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2eb81-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2eb81-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eb81-146">DirectXMath-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="2eb81-146">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="2eb81-147">DirectXMath-Releases</span><span class="sxs-lookup"><span data-stu-id="2eb81-147">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
