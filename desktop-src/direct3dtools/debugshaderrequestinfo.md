---
description: Stellt Informationen über eine Shader-Debuggeranforderung dar.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Debugshaderrequestinfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521587"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span data-ttu-id="35e38-103"><span id="vspixengine.debugshaderrequestinfo"></span>Debugshaderrequestinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="35e38-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo structure</span></span>

<span data-ttu-id="35e38-104">Stellt Informationen über eine Shader-Debuggeranforderung dar.</span><span class="sxs-lookup"><span data-stu-id="35e38-104">Represents information about a shader debugger request.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35e38-105">Syntax</span></span>


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a><span data-ttu-id="35e38-106">Member</span><span class="sxs-lookup"><span data-stu-id="35e38-106">Members</span></span>

<span data-ttu-id="35e38-107">**inszeniert**</span><span class="sxs-lookup"><span data-stu-id="35e38-107">**stage**</span></span>  
<span data-ttu-id="35e38-108">Die zu debuggende Pipeline Phase.</span><span class="sxs-lookup"><span data-stu-id="35e38-108">The pipeline stage to debug.</span></span>

<span data-ttu-id="35e38-109">**EventID**</span><span class="sxs-lookup"><span data-stu-id="35e38-109">**eventID**</span></span>  
<span data-ttu-id="35e38-110">Die ID des zu debuggenden Grafik Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="35e38-110">The ID of the graphics event to debug.</span></span>

<span data-ttu-id="35e38-111">**Framezahl**</span><span class="sxs-lookup"><span data-stu-id="35e38-111">**frameNumber**</span></span>  
<span data-ttu-id="35e38-112">Der zu debuggende Frame.</span><span class="sxs-lookup"><span data-stu-id="35e38-112">The frame to debug.</span></span>

<span data-ttu-id="35e38-113">**Vertex**</span><span class="sxs-lookup"><span data-stu-id="35e38-113">**vertex**</span></span>  
<span data-ttu-id="35e38-114">Der zu debuggende Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="35e38-114">The vertex to debug.</span></span>

<span data-ttu-id="35e38-115">**Megapixel**</span><span class="sxs-lookup"><span data-stu-id="35e38-115">**pixel**</span></span>  
<span data-ttu-id="35e38-116">Das zu debuggende Pixel.</span><span class="sxs-lookup"><span data-stu-id="35e38-116">The pixel to debug.</span></span>

<span data-ttu-id="35e38-117">**groupkoordinaten**</span><span class="sxs-lookup"><span data-stu-id="35e38-117">**groupCoordinates**</span></span>  
<span data-ttu-id="35e38-118">Die Koordinaten der Gruppe, die debuggt werden soll.</span><span class="sxs-lookup"><span data-stu-id="35e38-118">The coordinates of the group to debug.</span></span>

<span data-ttu-id="35e38-119">**Thread Koordinaten**</span><span class="sxs-lookup"><span data-stu-id="35e38-119">**threadCoordinates**</span></span>  
<span data-ttu-id="35e38-120">Die Koordinaten des zu debuggenden Threads.</span><span class="sxs-lookup"><span data-stu-id="35e38-120">The coordinates of the thread to debug</span></span>

## <a name="requirements"></a><span data-ttu-id="35e38-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35e38-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="35e38-122">Header</span><span class="sxs-lookup"><span data-stu-id="35e38-122">Header</span></span></p></td><td><span data-ttu-id="35e38-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="35e38-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



