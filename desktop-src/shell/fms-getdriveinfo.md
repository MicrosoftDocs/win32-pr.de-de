---
description: Enthält Informationen über das Laufwerk, das im aktiven Datei-Manager-Fenster ausgewählt wurde (das Verzeichnisfenster oder das Fenster Suchergebnisse).
title: FMS_GETDRIVEINFO-Struktur (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842231"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="7ffda-103">FMS \_ GETDRIVEINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="7ffda-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="7ffda-104">Enthält Informationen über das Laufwerk, das im aktiven Datei-Manager-Fenster ausgewählt wurde (das Verzeichnisfenster oder das Fenster Suchergebnisse).</span><span class="sxs-lookup"><span data-stu-id="7ffda-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ffda-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="7ffda-106">Member</span><span class="sxs-lookup"><span data-stu-id="7ffda-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ffda-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="7ffda-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="7ffda-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7ffda-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7ffda-109">Die Gesamtmenge des Speicherplatzes in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7ffda-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="7ffda-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="7ffda-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="7ffda-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7ffda-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7ffda-112">Die Menge des freien Speicherplatzes in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7ffda-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="7ffda-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="7ffda-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="7ffda-114">Typ: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="7ffda-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="7ffda-115">der mit NULL endende Pfad des aktuellen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="7ffda-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="7ffda-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="7ffda-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="7ffda-117">Typ: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="7ffda-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="7ffda-118">Die auf NULL endende Volumebezeichnung des Datenträgers, der dem Laufwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7ffda-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="7ffda-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="7ffda-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="7ffda-120">Typ: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="7ffda-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="7ffda-121">Der auf NULL endende Name der Netzwerkressource (wenn über ein Netzwerk auf das Laufwerk zugegriffen wird).</span><span class="sxs-lookup"><span data-stu-id="7ffda-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ffda-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ffda-122">Requirements</span></span>



| <span data-ttu-id="7ffda-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ffda-123">Requirement</span></span> | <span data-ttu-id="7ffda-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7ffda-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffda-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ffda-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7ffda-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ffda-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7ffda-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ffda-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7ffda-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ffda-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7ffda-129">Header</span><span class="sxs-lookup"><span data-stu-id="7ffda-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ffda-130"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="7ffda-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ffda-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ffda-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffda-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="7ffda-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="7ffda-133">**FM \_ GETDRIVEINFO**</span><span class="sxs-lookup"><span data-stu-id="7ffda-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




