---
description: Treiberfunktionsflag.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340119"
---
# <a name="d3denum"></a><span data-ttu-id="00b36-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="00b36-103">D3DENUM</span></span>

<span data-ttu-id="00b36-104">Treiberfunktionsflag.</span><span class="sxs-lookup"><span data-stu-id="00b36-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00b36-105">#definieren</span><span class="sxs-lookup"><span data-stu-id="00b36-105">#define</span></span></td>
<td><span data-ttu-id="00b36-106">Wert</span><span class="sxs-lookup"><span data-stu-id="00b36-106">Value</span></span></td>
<td><span data-ttu-id="00b36-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00b36-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00b36-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="00b36-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="00b36-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="00b36-109">0x00000002L</span></span></td>
<td><span data-ttu-id="00b36-110">Microsoft Windows Hardware Quality Labs (WHQL)-Treiber Tests.</span><span class="sxs-lookup"><span data-stu-id="00b36-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="00b36-111">Dabei handelt es sich um einen zeitaufwändigen Test, der eine einsekunde oder zwei Sekunden Zeitstrafen erfordert.</span><span class="sxs-lookup"><span data-stu-id="00b36-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="00b36-112">Diese Konstante wird vom whqllevel-Member von <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>verwendet.</span><span class="sxs-lookup"><span data-stu-id="00b36-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00b36-113">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="00b36-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="00b36-114">D3DENUM_WHQL_LEVEL ist für Direct3D9Ex, die unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder einem höheren Betriebssystem) ausgeführt werden, veraltet.</span><span class="sxs-lookup"><span data-stu-id="00b36-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="00b36-115">Eines dieser Betriebssysteme gibt 1 für den WHQL-Grad zurück, ohne den Status des Treibers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="00b36-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="00b36-116">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="00b36-116">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="00b36-117">Header</span><span class="sxs-lookup"><span data-stu-id="00b36-117">Header</span></span>                   | <span data-ttu-id="00b36-118">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="00b36-118">d3d9.h</span></span>     |
| <span data-ttu-id="00b36-119">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="00b36-119">Minimum operating system</span></span> | <span data-ttu-id="00b36-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="00b36-120">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="00b36-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00b36-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b36-122">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="00b36-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




