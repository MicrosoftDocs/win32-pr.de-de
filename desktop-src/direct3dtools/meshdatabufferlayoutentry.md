---
description: Stellt Informationen zu einem einzelnen Eintrag im Puffer Layout eines Netzes dar.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Meshdatabufferlayoutentry-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747576"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span data-ttu-id="48d89-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>Meshdatabufferlayoutentry-Struktur</span><span class="sxs-lookup"><span data-stu-id="48d89-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry structure</span></span>

<span data-ttu-id="48d89-104">Stellt Informationen zu einem einzelnen Eintrag im Puffer Layout eines Netzes dar.</span><span class="sxs-lookup"><span data-stu-id="48d89-104">Represents information about a single entry in the buffer layout of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48d89-105">Syntax</span></span>


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a><span data-ttu-id="48d89-106">Member</span><span class="sxs-lookup"><span data-stu-id="48d89-106">Members</span></span>

<span data-ttu-id="48d89-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="48d89-107">**pName**</span></span>  
<span data-ttu-id="48d89-108">Eine com-Zeichenfolge, die den Namen des Eintrags enthält.</span><span class="sxs-lookup"><span data-stu-id="48d89-108">A COM string containing the name of the entry.</span></span>

<span data-ttu-id="48d89-109">**numcomponents**</span><span class="sxs-lookup"><span data-stu-id="48d89-109">**numComponents**</span></span>  
<span data-ttu-id="48d89-110">Die Anzahl der homogenen Komponenten (Werte), aus denen dieser Eintrag besteht.</span><span class="sxs-lookup"><span data-stu-id="48d89-110">The number of homogenous components (values) that make up this entry.</span></span>

<span data-ttu-id="48d89-111">**isposition**</span><span class="sxs-lookup"><span data-stu-id="48d89-111">**isPosition**</span></span>  
<span data-ttu-id="48d89-112">true, wenn der Eintrag eine Position ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="48d89-112">true if the entry is a position; otherwise, false.</span></span>

<span data-ttu-id="48d89-113">**format**</span><span class="sxs-lookup"><span data-stu-id="48d89-113">**format**</span></span>  
<span data-ttu-id="48d89-114">Das Datenformat des Eintrags (Register).</span><span class="sxs-lookup"><span data-stu-id="48d89-114">The data format of the entry (register).</span></span> <span data-ttu-id="48d89-115">Weitere Informationen finden Sie unter Register \_ Format-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="48d89-115">For more information, see the REGISTER\_FORMAT enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="48d89-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48d89-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="48d89-117">Header</span><span class="sxs-lookup"><span data-stu-id="48d89-117">Header</span></span></p></td><td><span data-ttu-id="48d89-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="48d89-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



