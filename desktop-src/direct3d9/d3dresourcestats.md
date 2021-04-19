---
description: Ressourcen Statistik, die von D3DDEVINFO \_ ResourceManager erfasst wird, wenn der asynchrone Abfrage Mechanismus verwendet wird.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: D3DRESOURCESTATS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370408"
---
# <a name="d3dresourcestats-structure"></a><span data-ttu-id="4a276-103">D3DRESOURCESTATS-Struktur</span><span class="sxs-lookup"><span data-stu-id="4a276-103">D3DRESOURCESTATS structure</span></span>

<span data-ttu-id="4a276-104">Ressourcen Statistik, die von [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md) erfasst wird, wenn der asynchrone Abfrage Mechanismus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a276-104">Resource statistics gathered by the [**D3DDEVINFO\_ResourceManager**](d3ddevinfo-resourcemanager.md) when using the asynchronous query mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a276-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a276-105">Syntax</span></span>


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a><span data-ttu-id="4a276-106">Member</span><span class="sxs-lookup"><span data-stu-id="4a276-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a276-107">**bthrashing**</span><span class="sxs-lookup"><span data-stu-id="4a276-107">**bThrashing**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-108">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-109">Gibt an, ob eine Überlastung auftritt.</span><span class="sxs-lookup"><span data-stu-id="4a276-109">Indicates if thrashing is occurring.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-110">**Approxbytesherunter geladen**</span><span class="sxs-lookup"><span data-stu-id="4a276-110">**ApproxBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-112">Ungefähre Anzahl von Bytes, die vom Ressourcen-Manager heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="4a276-112">Approximate number of bytes downloaded by the resource manager.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-113">**Numevicts**</span><span class="sxs-lookup"><span data-stu-id="4a276-113">**NumEvicts**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-115">Anzahl der entfernten Objekte.</span><span class="sxs-lookup"><span data-stu-id="4a276-115">Number of objects evicted.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-116">**Numviderstellt**</span><span class="sxs-lookup"><span data-stu-id="4a276-116">**NumVidCreates**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-118">Anzahl von Objekten, die im Videospeicher erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4a276-118">Number of objects created in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-119">**Lastpri**</span><span class="sxs-lookup"><span data-stu-id="4a276-119">**LastPri**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-121">Priorität des letzten Objekts, das entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="4a276-121">Priority of last object evicted.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-122">**Numused**</span><span class="sxs-lookup"><span data-stu-id="4a276-122">**NumUsed**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-124">Anzahl von Objekten, die auf das Gerät festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="4a276-124">Number of objects set to the device.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-125">**Numusedinvidmem**</span><span class="sxs-lookup"><span data-stu-id="4a276-125">**NumUsedInVidMem**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-126">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-127">Anzahl der Objekte, die auf das Gerät festgelegt sind, die bereits im Videospeicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4a276-127">Number of objects set to the device, which are already in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-128">**Workingset**</span><span class="sxs-lookup"><span data-stu-id="4a276-128">**WorkingSet**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-129">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-129">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-130">Anzahl von Objekten im Videospeicher.</span><span class="sxs-lookup"><span data-stu-id="4a276-130">Number of objects in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-131">**Workingsetbytes**</span><span class="sxs-lookup"><span data-stu-id="4a276-131">**WorkingSetBytes**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-133">Anzahl von Bytes im Videospeicher.</span><span class="sxs-lookup"><span data-stu-id="4a276-133">Number of bytes in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-134">**Totalmanaged**</span><span class="sxs-lookup"><span data-stu-id="4a276-134">**TotalManaged**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-135">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-135">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-136">Die Gesamtanzahl verwalteter Objekte.</span><span class="sxs-lookup"><span data-stu-id="4a276-136">Total number of managed objects.</span></span>

</dd> <dt>

<span data-ttu-id="4a276-137">**TotalBytes**</span><span class="sxs-lookup"><span data-stu-id="4a276-137">**TotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="4a276-138">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a276-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4a276-139">Gesamtanzahl der Bytes von verwalteten Objekten.</span><span class="sxs-lookup"><span data-stu-id="4a276-139">Total number of bytes of managed objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a276-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a276-140">Requirements</span></span>



| <span data-ttu-id="4a276-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a276-141">Requirement</span></span> | <span data-ttu-id="4a276-142">Wert</span><span class="sxs-lookup"><span data-stu-id="4a276-142">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a276-143">Header</span><span class="sxs-lookup"><span data-stu-id="4a276-143">Header</span></span><br/> | <dl> <span data-ttu-id="4a276-144"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a276-144"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a276-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a276-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a276-146">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4a276-146">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="4a276-147">Asynchrone Benachrichtigung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4a276-147">Asynchronous Notification (Direct3D 9)</span></span>](asynchronous-notification.md)
</dt> </dl>

 

 
