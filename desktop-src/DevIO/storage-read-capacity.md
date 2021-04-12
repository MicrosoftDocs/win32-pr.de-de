---
description: Enthält Informationen zur Größe eines Geräts. Dies wird vom IOCTL- \_ Speicher \_ Lese- \_ Kapazitäts Steuerungs Code zurückgegeben.
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY Struktur (ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392990"
---
# <a name="storage_read_capacity-structure"></a><span data-ttu-id="34e7a-104">\_Kapazitäts Struktur zum Lesen des Speichers \_</span><span class="sxs-lookup"><span data-stu-id="34e7a-104">STORAGE\_READ\_CAPACITY structure</span></span>

<span data-ttu-id="34e7a-105">Enthält Informationen zur Größe eines Geräts.</span><span class="sxs-lookup"><span data-stu-id="34e7a-105">Contains information about the size of a device.</span></span> <span data-ttu-id="34e7a-106">Dies wird vom [**IOCTL- \_ Speicher \_ Lese- \_ Kapazitäts**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) Steuerungs Code zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34e7a-106">This is returned from the [**IOCTL\_STORAGE\_READ\_CAPACITY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e7a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="34e7a-107">Syntax</span></span>


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a><span data-ttu-id="34e7a-108">Member</span><span class="sxs-lookup"><span data-stu-id="34e7a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="34e7a-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="34e7a-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="34e7a-110">Die Version dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="34e7a-110">The version of this structure.</span></span> <span data-ttu-id="34e7a-111">Der Aufrufer muss diesen Member auf festlegen `sizeof(STORAGE_READ_CAPACITY)` .</span><span class="sxs-lookup"><span data-stu-id="34e7a-111">The caller must set this member to `sizeof(STORAGE_READ_CAPACITY)`.</span></span>

</dd> <dt>

<span data-ttu-id="34e7a-112">**Größe**</span><span class="sxs-lookup"><span data-stu-id="34e7a-112">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="34e7a-113">Die Größe der zurückgegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="34e7a-113">The size of the data returned.</span></span>

</dd> <dt>

<span data-ttu-id="34e7a-114">**Blocklength**</span><span class="sxs-lookup"><span data-stu-id="34e7a-114">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="34e7a-115">Die Anzahl der Bytes pro Block.</span><span class="sxs-lookup"><span data-stu-id="34e7a-115">The number of bytes per block.</span></span>

</dd> <dt>

<span data-ttu-id="34e7a-116">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="34e7a-116">**NumberOfBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="34e7a-117">Die Gesamtanzahl der Blöcke auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="34e7a-117">The total number of blocks on the disk.</span></span>

</dd> <dt>

<span data-ttu-id="34e7a-118">**Disklength**</span><span class="sxs-lookup"><span data-stu-id="34e7a-118">**DiskLength**</span></span>
</dt> <dd>

<span data-ttu-id="34e7a-119">Die Datenträger Größe in Byte.</span><span class="sxs-lookup"><span data-stu-id="34e7a-119">The disk size in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34e7a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34e7a-120">Remarks</span></span>

<span data-ttu-id="34e7a-121">Die Header Datei "ntddstor. h" ist im Windows-Treiberkit (WDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34e7a-121">The header file Ntddstor.h is available in the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="34e7a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34e7a-122">Requirements</span></span>



| <span data-ttu-id="34e7a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34e7a-123">Requirement</span></span> | <span data-ttu-id="34e7a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="34e7a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34e7a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34e7a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="34e7a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34e7a-126">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="34e7a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34e7a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="34e7a-128">Windows Server 2008, Windows Server 2003 mit SP1</span><span class="sxs-lookup"><span data-stu-id="34e7a-128">Windows Server 2008, Windows Server 2003 with SP1</span></span><br/>                          |
| <span data-ttu-id="34e7a-129">Header</span><span class="sxs-lookup"><span data-stu-id="34e7a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="34e7a-130"><dt>Ntddstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e7a-130"><dt>Ntddstor.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e7a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34e7a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e7a-132">**IOCTL- \_ Speicher \_ Lese \_ Kapazität**</span><span class="sxs-lookup"><span data-stu-id="34e7a-132">**IOCTL\_STORAGE\_READ\_CAPACITY**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




