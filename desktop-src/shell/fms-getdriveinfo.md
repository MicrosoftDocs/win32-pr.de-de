---
description: Enthält Informationen über das im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse") ausgewählte Laufwerk.
title: FMS_GETDRIVEINFO-Struktur (WF. h)
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
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979697"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="c1255-103">FMS \_ getdriveingefo-Struktur</span><span class="sxs-lookup"><span data-stu-id="c1255-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="c1255-104">Enthält Informationen über das im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse") ausgewählte Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="c1255-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1255-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1255-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="c1255-106">Member</span><span class="sxs-lookup"><span data-stu-id="c1255-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1255-107">**dwtotalspace**</span><span class="sxs-lookup"><span data-stu-id="c1255-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="c1255-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c1255-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c1255-109">Die Gesamtmenge des Speicherplatzes in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c1255-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="c1255-110">**dwfreespace**</span><span class="sxs-lookup"><span data-stu-id="c1255-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="c1255-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c1255-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c1255-112">Der freie Speicherplatz in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c1255-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="c1255-113">**szpath**</span><span class="sxs-lookup"><span data-stu-id="c1255-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="c1255-114">Typ: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="c1255-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="c1255-115">der NULL terminierte Pfad des aktuellen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="c1255-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="c1255-116">**szvolume**</span><span class="sxs-lookup"><span data-stu-id="c1255-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="c1255-117">Typ: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="c1255-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="c1255-118">Die mit NULL terminierte Volumebezeichnung des Datenträgers, der dem Laufwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c1255-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="c1255-119">**szshare**</span><span class="sxs-lookup"><span data-stu-id="c1255-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="c1255-120">Typ: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="c1255-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="c1255-121">Der NULL-terminierte Name der Netzwerkressource (wenn über ein Netzwerk auf das Laufwerk zugegriffen wird).</span><span class="sxs-lookup"><span data-stu-id="c1255-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1255-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c1255-122">Requirements</span></span>



| <span data-ttu-id="c1255-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1255-123">Requirement</span></span> | <span data-ttu-id="c1255-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c1255-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1255-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1255-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c1255-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1255-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c1255-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1255-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c1255-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1255-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1255-129">Header</span><span class="sxs-lookup"><span data-stu-id="c1255-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1255-130"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1255-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1255-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c1255-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1255-132">**"F"**</span><span class="sxs-lookup"><span data-stu-id="c1255-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="c1255-133">**FM \_ getdriveingefo**</span><span class="sxs-lookup"><span data-stu-id="c1255-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




