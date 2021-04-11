---
description: Gibt die Mesh-Daten abzüglich der Positionsdaten an.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: "\"F\"-Daten"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123854"
---
# <a name="fvfdata"></a><span data-ttu-id="83453-103">"F"-Daten</span><span class="sxs-lookup"><span data-stu-id="83453-103">FVFData</span></span>

<span data-ttu-id="83453-104">Gibt die Mesh-Daten abzüglich der Positionsdaten an.</span><span class="sxs-lookup"><span data-stu-id="83453-104">Specifies the mesh data minus the position data.</span></span>

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="83453-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="83453-105">Where:</span></span>

-   <span data-ttu-id="83453-106">DWF VF: ein f-Code.</span><span class="sxs-lookup"><span data-stu-id="83453-106">dwFVF - A FVF code.</span></span>
-   <span data-ttu-id="83453-107">ndwords: Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="83453-107">nDWords - Binary data.</span></span> <span data-ttu-id="83453-108">Die Anzahl der DWORDs.</span><span class="sxs-lookup"><span data-stu-id="83453-108">The number of DWORDS.</span></span>
-   <span data-ttu-id="83453-109">Data \[ ndwords \] : Array von DWords, die die Daten in jedem Scheitelpunkt Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="83453-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="83453-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83453-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83453-111">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="83453-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



