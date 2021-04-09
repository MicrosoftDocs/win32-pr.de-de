---
description: Stellt eine Beschreibung eines Textur Slice dar.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixenginetextureslicedescriptor-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123980"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span data-ttu-id="eb38b-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>Pixenginetextureslicedescriptor-Struktur</span><span class="sxs-lookup"><span data-stu-id="eb38b-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor structure</span></span>

<span data-ttu-id="eb38b-104">Stellt eine Beschreibung eines Textur Slice dar.</span><span class="sxs-lookup"><span data-stu-id="eb38b-104">Represents a description of a texture slice.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb38b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb38b-105">Syntax</span></span>


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a><span data-ttu-id="eb38b-106">Member</span><span class="sxs-lookup"><span data-stu-id="eb38b-106">Members</span></span>

<span data-ttu-id="eb38b-107">**width**</span><span class="sxs-lookup"><span data-stu-id="eb38b-107">**width**</span></span>  
<span data-ttu-id="eb38b-108">Die Breite (Anzahl der Stichproben in der X-Achse) des Slice.</span><span class="sxs-lookup"><span data-stu-id="eb38b-108">The width (number of samples in the X axis) of the slice.</span></span>

<span data-ttu-id="eb38b-109">**height**</span><span class="sxs-lookup"><span data-stu-id="eb38b-109">**height**</span></span>  
<span data-ttu-id="eb38b-110">Die Höhe (Anzahl der Stichproben auf der Y-Achse) des Slice.</span><span class="sxs-lookup"><span data-stu-id="eb38b-110">The height (number of samples in the Y axis) of the slice.</span></span>

<span data-ttu-id="eb38b-111">**blockrowbytes**</span><span class="sxs-lookup"><span data-stu-id="eb38b-111">**blockRowBytes**</span></span>  
<span data-ttu-id="eb38b-112">Die Anzahl der Bytes pro Zeile in jedem Block.</span><span class="sxs-lookup"><span data-stu-id="eb38b-112">The number of bytes per row in each block.</span></span>

<span data-ttu-id="eb38b-113">**offset**</span><span class="sxs-lookup"><span data-stu-id="eb38b-113">**offset**</span></span>  
<span data-ttu-id="eb38b-114">Der Offset des Slice innerhalb der gesamten Textur.</span><span class="sxs-lookup"><span data-stu-id="eb38b-114">The offset of the slice within the whole texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb38b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb38b-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eb38b-116">Header</span><span class="sxs-lookup"><span data-stu-id="eb38b-116">Header</span></span></p></td><td><span data-ttu-id="eb38b-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eb38b-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



