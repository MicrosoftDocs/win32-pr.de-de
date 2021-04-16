---
description: Definiert eine GUID, die in anderen Vorlagen verwendet werden kann.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521432"
---
# <a name="guid-directx-9"></a><span data-ttu-id="2c94d-103">GUID (DirectX 9)</span><span class="sxs-lookup"><span data-stu-id="2c94d-103">Guid (DirectX 9)</span></span>

<span data-ttu-id="2c94d-104">Definiert eine GUID, die in anderen Vorlagen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c94d-104">Defines a GUID that can be used in other templates.</span></span>

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

<span data-ttu-id="2c94d-105">Dabei bilden die Parameter zusammen das binäre Speicherformat für eine GUID:</span><span class="sxs-lookup"><span data-stu-id="2c94d-105">Where the parameters together form the binary storage format for a GUID:</span></span>

-   <span data-ttu-id="2c94d-106">data1-32-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="2c94d-106">data1 - 32-bit unsigned integer data value</span></span>
-   <span data-ttu-id="2c94d-107">data2-16-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="2c94d-107">data2 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="2c94d-108">data3-16-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="2c94d-108">data3 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="2c94d-109">data4-ein Array nicht signierter Zeichen</span><span class="sxs-lookup"><span data-stu-id="2c94d-109">data4 - An array of unsigned characters</span></span>

## <a name="see-also"></a><span data-ttu-id="2c94d-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c94d-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c94d-111">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="2c94d-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



