---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351999"
---
# <a name="directxmath"></a><span data-ttu-id="05c42-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="05c42-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="05c42-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="05c42-104">Purpose</span></span>

<span data-ttu-id="05c42-105">Die directxmath-API bietet SIMD-freundliche C++-Typen und-Funktionen für häufige lineare Algebra-und Grafik mathematische Operationen, die für DirectX-Anwendungen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="05c42-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="05c42-106">Die Bibliothek bietet optimierte Versionen für Windows 32-Bit (x86), Windows 64-Bit (x64) und Windows auf Arm/ARM64 durch SSE, AVX und systeminterne Unterstützung für Arm-Neon im Visual C++ Compiler.</span><span class="sxs-lookup"><span data-stu-id="05c42-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="05c42-107">Für Entwickler, die noch nicht mit directxmath vertraut sind, sollten Sie den simplemath-Wrapper im *DirectX-Toolkit* für [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) als Ausgangspunkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="05c42-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="05c42-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="05c42-108">In this section</span></span>



| <span data-ttu-id="05c42-109">Thema</span><span class="sxs-lookup"><span data-stu-id="05c42-109">Topic</span></span>                                                                     | <span data-ttu-id="05c42-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05c42-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="05c42-111">Directxmath-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="05c42-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="05c42-112">Directxmath bietet eine mathematische Lösung, die für Windows optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="05c42-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="05c42-113">Directxmath-Programmier Referenz</span><span class="sxs-lookup"><span data-stu-id="05c42-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="05c42-114">Dieser Abschnitt enthält Referenzmaterial für die directxmath-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="05c42-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="05c42-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="05c42-115">Developer audience</span></span>

<span data-ttu-id="05c42-116">Die directxmath-Bibliothek ist für C++-Entwickler konzipiert, die an spielen und DirectX-Grafiken in Windows Store-Apps, Xbox-spielen und herkömmlichen Desktop-Apps für Windows arbeiten.</span><span class="sxs-lookup"><span data-stu-id="05c42-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="05c42-117">Abrufen von directxmath</span><span class="sxs-lookup"><span data-stu-id="05c42-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="05c42-118">Die directxmath-Header werden in der Windows SDK geliefert, die in Visual Studio 2012 oder höher enthalten ist, und als alle Inline Header gibt es keine DLL oder statische Bibliothek, mit der eine Verknüpfung hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="05c42-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="05c42-119">Es ist auch als Paket auf [nuget](https://www.nuget.org/packages/directxmath/)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05c42-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="05c42-120">Directxmath ist Open Source unter der [mit-Lizenz](https://opensource.org/licenses/MIT) , die auf [GitHub](https://github.com/Microsoft/DirectXMath)gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="05c42-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




