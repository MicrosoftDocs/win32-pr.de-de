---
description: Enthält die Seriennummer eines USB-Geräts. Sie wird vom IOCTL- \_ Speicher \_ Ablaufsteuerungs-Code für \_ Medien \_ Seriennummern verwendet \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: MEDIA_SERIAL_NUMBER_DATA Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355711"
---
# <a name="media_serial_number_data-structure"></a><span data-ttu-id="814f9-104">\_Datenstruktur der Medien Serien \_ Nummer \_</span><span class="sxs-lookup"><span data-stu-id="814f9-104">MEDIA\_SERIAL\_NUMBER\_DATA structure</span></span>

<span data-ttu-id="814f9-105">Enthält die Seriennummer eines USB-Geräts.</span><span class="sxs-lookup"><span data-stu-id="814f9-105">Contains the serial number of a USB device.</span></span> <span data-ttu-id="814f9-106">Sie wird vom ioctl-Speicher Ablaufsteuerungs-Code für [**\_ \_ \_ Medien \_ Serien \_ Nummern**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) verwendet.</span><span class="sxs-lookup"><span data-stu-id="814f9-106">It is used by the [**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="814f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="814f9-107">Syntax</span></span>


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a><span data-ttu-id="814f9-108">Member</span><span class="sxs-lookup"><span data-stu-id="814f9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="814f9-109">**Serialzahldauer**</span><span class="sxs-lookup"><span data-stu-id="814f9-109">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="814f9-110">Die Größe der **serialnummeri-Daten** Zeichenfolge in Bytes.</span><span class="sxs-lookup"><span data-stu-id="814f9-110">The size of the **SerialNumberData** string, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="814f9-111">**Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="814f9-111">**Result**</span></span>
</dt> <dd>

<span data-ttu-id="814f9-112">Der Status der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="814f9-112">The status of the request.</span></span>

</dd> <dt>

<span data-ttu-id="814f9-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="814f9-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="814f9-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="814f9-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="814f9-115">**Serialzahldaten**</span><span class="sxs-lookup"><span data-stu-id="814f9-115">**SerialNumberData**</span></span>
</dt> <dd>

<span data-ttu-id="814f9-116">Die Seriennummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="814f9-116">The serial number of the device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="814f9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="814f9-117">Remarks</span></span>

<span data-ttu-id="814f9-118">Für die Datenstruktur der **Medien \_ Serien \_ Nummer \_** ist keine Header Datei verfügbar.</span><span class="sxs-lookup"><span data-stu-id="814f9-118">No header file is available for the **MEDIA\_SERIAL\_NUMBER\_DATA** structure.</span></span> <span data-ttu-id="814f9-119">Fügen Sie die Struktur Definition am oberen Rand dieser Seite in den Quellcode ein.</span><span class="sxs-lookup"><span data-stu-id="814f9-119">Include the structure definition at the top of this page in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="814f9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="814f9-120">Requirements</span></span>



| <span data-ttu-id="814f9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="814f9-121">Requirement</span></span> | <span data-ttu-id="814f9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="814f9-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="814f9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="814f9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="814f9-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="814f9-124">Windows XP</span></span><br/>          |
| <span data-ttu-id="814f9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="814f9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="814f9-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="814f9-126">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="814f9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="814f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814f9-128">**IOCTL- \_ Speicher \_ Medien- \_ \_ Serien \_ Nummer**</span><span class="sxs-lookup"><span data-stu-id="814f9-128">**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




