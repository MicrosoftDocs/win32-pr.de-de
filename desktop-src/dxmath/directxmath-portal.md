---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd35f1faf004bc55a6802da204a6c2fe4e7869b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113008"
---
# <a name="directxmath"></a><span data-ttu-id="3c784-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="3c784-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="3c784-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="3c784-104">Purpose</span></span>

<span data-ttu-id="3c784-105">Die DirectXMath-API stellt SIMD-freundliche C++-Typen und -Funktionen für gängige lineare Algebra- und Grafikoperationen bereit, die für DirectX-Anwendungen üblich sind.</span><span class="sxs-lookup"><span data-stu-id="3c784-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="3c784-106">Die Bibliothek bietet optimierte Versionen für systeminterne Windows 32-Bit-Versionen (x86), Windows 64-Bit (x64) und Windows unter ARM/ARM64 über SSE-, AVX- und ARM-NEON-Unterstützung im Visual C++-Compiler.</span><span class="sxs-lookup"><span data-stu-id="3c784-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="3c784-107">Für Entwickler, die noch nicht mit DirectXMath beginnen, sollten Sie erwägen, den SimpleMath-Wrapper im *DirectX Tool Kit* für [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) als Ausgangspunkt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c784-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3c784-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3c784-108">In this section</span></span>



| <span data-ttu-id="3c784-109">Thema</span><span class="sxs-lookup"><span data-stu-id="3c784-109">Topic</span></span>                                                                     | <span data-ttu-id="3c784-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c784-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="3c784-111">DirectXMath-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="3c784-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="3c784-112">DirectXMath bietet eine für Windows optimierte mathematische Lösung.</span><span class="sxs-lookup"><span data-stu-id="3c784-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="3c784-113">DirectXMath-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="3c784-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="3c784-114">Dieser Abschnitt enthält Referenzmaterial für die DirectXMath-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="3c784-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="3c784-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="3c784-115">Developer audience</span></span>

<span data-ttu-id="3c784-116">Die DirectXMath-Bibliothek ist für C++-Entwickler konzipiert, die an Spielen und DirectX-Grafiken in Windows Store-Apps, Xbox-Spielen und herkömmlichen Desktop-Apps für Windows arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c784-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="3c784-117">Abrufen von DirectXMath</span><span class="sxs-lookup"><span data-stu-id="3c784-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="3c784-118">Die DirectXMath-Header sind im Windows SDK enthalten, die Visual Studio 2012 oder höher enthalten sind, und als All-Inline-Header gibt es keine DLL oder statische Bibliothek, mit der eine Verknüpfung erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3c784-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="3c784-119">Es ist auch als Paket auf [NuGet verfügbar.](https://www.nuget.org/packages/directxmath/)</span><span class="sxs-lookup"><span data-stu-id="3c784-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="3c784-120">DirectXMath ist open source unter der [AUF GitHub](https://opensource.org/licenses/MIT) gehosteten [MIT-Lizenz.](https://github.com/Microsoft/DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="3c784-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




