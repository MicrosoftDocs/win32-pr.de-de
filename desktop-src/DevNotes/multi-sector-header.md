---
description: Stellt den multisektorheader dar.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: MULTI_SECTOR_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747881"
---
# <a name="multi_sector_header-structure"></a><span data-ttu-id="24b73-103">\_Multisektor- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="24b73-103">MULTI\_SECTOR\_HEADER structure</span></span>

<span data-ttu-id="24b73-104">\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]</span><span class="sxs-lookup"><span data-stu-id="24b73-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="24b73-105">Stellt den multisektorheader dar.</span><span class="sxs-lookup"><span data-stu-id="24b73-105">Represents the multisector header.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b73-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="24b73-106">Syntax</span></span>


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a><span data-ttu-id="24b73-107">Member</span><span class="sxs-lookup"><span data-stu-id="24b73-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="24b73-108">**Signature**</span><span class="sxs-lookup"><span data-stu-id="24b73-108">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="24b73-109">Die Signatur.</span><span class="sxs-lookup"><span data-stu-id="24b73-109">The signature.</span></span> <span data-ttu-id="24b73-110">Dieser Wert ist für den Benutzer benutzerfreundlicher.</span><span class="sxs-lookup"><span data-stu-id="24b73-110">This value is a convenience to the user.</span></span>

</dd> <dt>

<span data-ttu-id="24b73-111">**Updatesequencearrayoffset**</span><span class="sxs-lookup"><span data-stu-id="24b73-111">**UpdateSequenceArrayOffset**</span></span>
</dt> <dd>

<span data-ttu-id="24b73-112">Der Offset des Update Sequenz Arrays vom Anfang dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="24b73-112">The offset to the update sequence array, from the start of this structure.</span></span> <span data-ttu-id="24b73-113">Das Update Sequenz Array muss vor dem letzten ushort-Wert des ersten Sektors enden.</span><span class="sxs-lookup"><span data-stu-id="24b73-113">The update sequence array must end before the last USHORT value in the first sector.</span></span>

</dd> <dt>

<span data-ttu-id="24b73-114">**Updatesequencearraysize**</span><span class="sxs-lookup"><span data-stu-id="24b73-114">**UpdateSequenceArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="24b73-115">Die Größe des Update Sequenz Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="24b73-115">The size of the update sequence array, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24b73-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24b73-116">Remarks</span></span>

<span data-ttu-id="24b73-117">Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.</span><span class="sxs-lookup"><span data-stu-id="24b73-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="24b73-118">Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.</span><span class="sxs-lookup"><span data-stu-id="24b73-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="24b73-119">Der multisektorheader und das Update Sequenz Array ermöglichen die Erkennung unvollständiger multisektorübertragungen für Geräte, die eine physische Sektorgröße aufweisen, die größer oder gleich der Sequenznummer Stride (512) ist, oder die keine Sektoren außerhalb der Reihenfolge übertragen.</span><span class="sxs-lookup"><span data-stu-id="24b73-119">The multisector header and update sequence array provide detection of incomplete multisector transfers for devices that either have a physical sector size greater than or equal to the sequence number stride (512) or that do not transfer sectors out of order.</span></span> <span data-ttu-id="24b73-120">Wenn ein Gerät vorhanden ist, dessen Sektorgröße kleiner ist als die Sequenznummer, und in einigen Fällen Sektoren außerhalb der Reihenfolge übermittelt werden, bietet das Update Sequenz Array keine absolute Erkennung unvollständiger Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="24b73-120">If a device exists that has a sector size smaller than the sequence number stride and it sometimes transfers sectors out of order, then the update sequence array will not provide absolute detection of incomplete transfers.</span></span> <span data-ttu-id="24b73-121">Die Sequenznummer Stride wird auf eine kleine Zahl festgelegt, um den absoluten Schutz für alle bekannten Festplatten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="24b73-121">The sequence number stride is set to a small enough number to provide absolute protection for all known hard disks.</span></span> <span data-ttu-id="24b73-122">Der Wert ist nicht kleiner, oder es kann zu einer übermäßigen Laufzeit oder mehr Aufwand kommen.</span><span class="sxs-lookup"><span data-stu-id="24b73-122">It is not set any smaller or there might be excessive run time or space overhead.</span></span>

<span data-ttu-id="24b73-123">Das Update Sequenz Array besteht aus einem Array von *n* **UShort** -Werten, wobei *n* die Größe der geschützten Struktur ist, dividiert durch die Sequenznummer Stride.</span><span class="sxs-lookup"><span data-stu-id="24b73-123">The update sequence array consists of an array of *n* **USHORT** values, where *n* is the size of the structure being protected divided by the sequence number stride.</span></span> <span data-ttu-id="24b73-124">Das erste Wort enthält die Aktualisierungs Sequenznummer, bei der es sich um einen zyklischen gegen Wert handelt, mit dem die Anzahl der in die enthaltenden Struktur auf den Datenträger geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="24b73-124">The first word contains the update sequence number, which is a cyclical counter of the number of times the containing structure has been written to disk.</span></span> <span data-ttu-id="24b73-125">Im nächsten Schritt werden die *n* gespeicherten **UShort** -Werte, die von der Update Sequenznummer beim letzten Schreiben der enthaltenden Struktur auf den Datenträger überschrieben wurden, überschrieben.</span><span class="sxs-lookup"><span data-stu-id="24b73-125">Next are the *n* saved **USHORT** values that were overwritten by the update sequence number the last time the containing structure was written to disk.</span></span>

<span data-ttu-id="24b73-126">Jedes Mal, wenn die geschützte Struktur in den Datenträger geschrieben wird, wird das letzte Wort in jeder Sequenznummern Sequenz an der jeweiligen Position im Sequenznummern Array gespeichert und mit der nächsten Update Sequenznummer überschrieben.</span><span class="sxs-lookup"><span data-stu-id="24b73-126">Each time the protected structure is about to be written to disk, the last word in each sequence number stride is saved to its respective position in the sequence number array, then it is overwritten with the next update sequence number.</span></span> <span data-ttu-id="24b73-127">Nach dem Schreiben oder immer dann, wenn die Struktur gelesen wird, wird das gespeicherte Wort aus dem Sequenznummern Array an seine tatsächliche Position in der Struktur wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="24b73-127">After the write, or whenever the structure is read, the saved word from the sequence number array is restored to its actual position in the structure.</span></span> <span data-ttu-id="24b73-128">Vor dem Wiederherstellen der gespeicherten Wörter bei Lesevorgängen werden alle Sequenznummern am Ende jedes Stride mit der tatsächlichen Sequenznummer am Anfang des Arrays verglichen.</span><span class="sxs-lookup"><span data-stu-id="24b73-128">Before restoring the saved words on reads, all the sequence numbers at the end of each stride are compared with the actual sequence number at the start of the array.</span></span> <span data-ttu-id="24b73-129">Wenn einer dieser Vergleiche nicht gleich ist, wurde eine fehlgeschlagene multisektorübertragung erkannt.</span><span class="sxs-lookup"><span data-stu-id="24b73-129">If any of these comparisons are not equal, then a failed multisector transfer has been detected.</span></span>

<span data-ttu-id="24b73-130">Die Größe des Arrays wird durch die Größe der enthaltenden Struktur bestimmt.</span><span class="sxs-lookup"><span data-stu-id="24b73-130">The size of the array is determined by the size of the containing structure.</span></span> <span data-ttu-id="24b73-131">Das Update Sequenz Array sollte am Ende des Headers der Struktur eingeschlossen werden, die er aufgrund seiner Variablen Größe schützt.</span><span class="sxs-lookup"><span data-stu-id="24b73-131">The update sequence array should be included at the end of the header of the structure it is protecting because of its variable size.</span></span> <span data-ttu-id="24b73-132">Der Benutzer muss sicherstellen, dass der richtige Speicherplatz für die enthaltende Struktur reserviert ist: (Größe von Structure/512 + 1) \* sizeof (UShort).</span><span class="sxs-lookup"><span data-stu-id="24b73-132">The user must ensure that the correct space is reserved for the containing structure: (size of structure / 512 + 1) \* sizeof(USHORT).</span></span>

## <a name="see-also"></a><span data-ttu-id="24b73-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24b73-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b73-134">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="24b73-134">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
