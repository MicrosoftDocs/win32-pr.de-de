---
description: Treiberfunktionsflag.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829d03bf596c24bfb6b3443ace859629f723a664
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343256"
---
# <a name="d3denum"></a><span data-ttu-id="e9ac2-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="e9ac2-103">D3DENUM</span></span>

<span data-ttu-id="e9ac2-104">Treiberfunktionsflag.</span><span class="sxs-lookup"><span data-stu-id="e9ac2-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9ac2-105">#Definieren</span><span class="sxs-lookup"><span data-stu-id="e9ac2-105">#define</span></span></td>
<td><span data-ttu-id="e9ac2-106">Wert</span><span class="sxs-lookup"><span data-stu-id="e9ac2-106">Value</span></span></td>
<td><span data-ttu-id="e9ac2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9ac2-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9ac2-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="e9ac2-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="e9ac2-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="e9ac2-109">0x00000002L</span></span></td>
<td><span data-ttu-id="e9ac2-110">Testen von Microsoft Windows Hardware Quality Labs-Treibern (WHQL).</span><span class="sxs-lookup"><span data-stu-id="e9ac2-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="e9ac2-111">Dies ist ein zeitaufwändiger Test, der eine Zeiteinbuße von einer Sekunde oder zwei Sekunden erfordert.</span><span class="sxs-lookup"><span data-stu-id="e9ac2-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="e9ac2-112">Diese Konstante wird vom WHQLLevel-Member von <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9ac2-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9ac2-113">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="e9ac2-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="e9ac2-114">D3DENUM_WHQL_LEVEL ist für Direct3D9Ex unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder einem aktuelleren Betriebssystem) veraltet.</span><span class="sxs-lookup"><span data-stu-id="e9ac2-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="e9ac2-115">Jedes dieser Betriebssysteme gibt 1 für die WHQL-Ebene zurück, ohne den Status des Treibers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e9ac2-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="e9ac2-116">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="e9ac2-116">Constant Information</span></span>



| <span data-ttu-id="e9ac2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9ac2-117">Requirement</span></span>                         | <span data-ttu-id="e9ac2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e9ac2-118">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="e9ac2-119">Header</span><span class="sxs-lookup"><span data-stu-id="e9ac2-119">Header</span></span>                   | <span data-ttu-id="e9ac2-120">d3d9.h</span><span class="sxs-lookup"><span data-stu-id="e9ac2-120">d3d9.h</span></span>     |
| <span data-ttu-id="e9ac2-121">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="e9ac2-121">Minimum operating system</span></span> | <span data-ttu-id="e9ac2-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e9ac2-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e9ac2-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9ac2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ac2-124">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e9ac2-124">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




