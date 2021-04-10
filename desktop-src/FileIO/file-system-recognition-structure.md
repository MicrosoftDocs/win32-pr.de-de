---
description: Enthält die Informationen auf dem Datenträger, die im Startsektor für Volumes gespeichert sind (logischer Datenträger Sektor null).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: FILE_SYSTEM_RECOGNITION_STRUCTURE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042021"
---
# <a name="file_system_recognition_structure-structure"></a><span data-ttu-id="bd7a5-103">Struktur der Datei \_ System \_ Erkennungs \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="bd7a5-103">FILE\_SYSTEM\_RECOGNITION\_STRUCTURE structure</span></span>

<span data-ttu-id="bd7a5-104">Enthält die Informationen auf dem Datenträger, die im Startsektor des Volumes gespeichert sind (logischer Datenträger Sektor null).</span><span class="sxs-lookup"><span data-stu-id="bd7a5-104">Contains the on-disk file system recognition information stored in the volume's boot sector (logical disk sector zero).</span></span>

<span data-ttu-id="bd7a5-105">Dabei handelt es sich um eine intern definierte Datenstruktur, die nicht in einem öffentlichen Header verfügbar ist und hier für Dateisystem Entwickler bereitgestellt wird, die die Dateisystem Erkennung nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-105">This is an internally-defined data structure not available in a public header and is provided here for file system developers who want to take advantage of file system recognition.</span></span> <span data-ttu-id="bd7a5-106">Weitere Informationen finden Sie unter [Datei System Erkennung](file-system-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="bd7a5-106">For more information, see [File System Recognition](file-system-recognition.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd7a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd7a5-107">Syntax</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a><span data-ttu-id="bd7a5-108">Member</span><span class="sxs-lookup"><span data-stu-id="bd7a5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd7a5-109">**"Jmp"**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-109">**Jmp**</span></span>
</dt> <dd>

<span data-ttu-id="bd7a5-110">Die jmp-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-110">The JMP instruction.</span></span> <span data-ttu-id="bd7a5-111">Dieser Datenmember ist nicht in dem Wert enthalten, der im **Prüfsummen** Datenmember enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-111">This data member is not included in the value contained in the **Checksum** data member.</span></span>

</dd> <dt>

<span data-ttu-id="bd7a5-112">**FSName**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-112">**FsName**</span></span>
</dt> <dd>

<span data-ttu-id="bd7a5-113">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-113">The file system name.</span></span> <span data-ttu-id="bd7a5-114">Dabei handelt es sich um eine Sequenz von 8 ASCII-Zeichen, die den nicht lokalisierbaren lesbaren Namen des Dateisystems darstellt, mit dem das Volume formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-114">This is a sequence of 8 ASCII characters that represents the nonlocalizable human-readable name of the file system the volume is formatted with.</span></span>

<span data-ttu-id="bd7a5-115">Diese Zeichenfolge befindet sich am gleichen Speicherort wie der OEM-Dateisystem Name auf einem Datenträger mit einer normalen BPB-Struktur (BIOS Parameter Block).</span><span class="sxs-lookup"><span data-stu-id="bd7a5-115">This string is in the same place as the OEM file system name on a disk with a normal BIOS parameter block (BPB) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bd7a5-116">**Mustbezero**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-116">**MustBeZero**</span></span>
</dt> <dd>

<span data-ttu-id="bd7a5-117">Reservierter Speicherplatz, der alle Nullen enthält.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-117">Reserved space that contains all zeros.</span></span>

<span data-ttu-id="bd7a5-118">Dieser Datenmember überlappt, was normalerweise die folgenden Datenmember in einer BPB sind:</span><span class="sxs-lookup"><span data-stu-id="bd7a5-118">This data member overlaps what normally are the following data members in a BPB:</span></span>

-   <span data-ttu-id="bd7a5-119">**Bytespersektor**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-119">**BytesPerSector**</span></span>
-   <span data-ttu-id="bd7a5-120">**Sector-Cluster**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-120">**SectorsPerCluster**</span></span>
-   <span data-ttu-id="bd7a5-121">**Reservedsector count**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-121">**ReservedSectorCount**</span></span>

<span data-ttu-id="bd7a5-122">Da diese Datenmember auf 0 (null) festgelegt sind, sollte dies ausreichen, um zu bewirken, dass frühere Betriebssysteme den Schluss haben, dass es sich nicht um ein gültiges BPB handelt und daher das Volume erkannt</span><span class="sxs-lookup"><span data-stu-id="bd7a5-122">Because these data members are set to zero, this should be sufficient to cause earlier OSs to conclude that this is not a valid BPB and therefore recognize the volume.</span></span>

</dd> <dt>

<span data-ttu-id="bd7a5-123">**Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-123">**Identifier**</span></span>
</dt> <dd>

<span data-ttu-id="bd7a5-124">Ein Strukturbezeichner.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-124">A structure identifier.</span></span> <span data-ttu-id="bd7a5-125">Muss den in Little-Endian-Byte Reihenfolge angeordneten Wert 0x53525346 enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-125">Must contain the value 0x53525346 arranged in little-endian byte order.</span></span>

<span data-ttu-id="bd7a5-126">An dieser Stelle in der Struktur werden die Daten auf 16 Bytes ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-126">At this point in the structure, the data is aligned to 16 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bd7a5-127">**Länge**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-127">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="bd7a5-128">Die Anzahl der Bytes in dieser-Struktur von Anfang bis Ende, einschließlich des **jmp** -Datenelements.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-128">The number of bytes in this structure, from the beginning to the end, including the **Jmp** data member.</span></span>

</dd> <dt>

<span data-ttu-id="bd7a5-129">**Prüfsumme**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-129">**Checksum**</span></span>
</dt> <dd>

<span data-ttu-id="bd7a5-130">Eine 2-Byte-Prüfsumme, die über die Bytes beginnend mit dem **FSName** -Datenmember berechnet wird und mit dem letzten Byte dieser Struktur endet, ausgenommen der **jmp** -und **Prüfsumme** -Datenmember.</span><span class="sxs-lookup"><span data-stu-id="bd7a5-130">A two-byte checksum calculated over the bytes starting at the **FsName** data member and ending at the last byte of this structure, excluding the **Jmp** and **Checksum** data members.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd7a5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd7a5-131">Requirements</span></span>



| <span data-ttu-id="bd7a5-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd7a5-132">Requirement</span></span> | <span data-ttu-id="bd7a5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="bd7a5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bd7a5-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd7a5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bd7a5-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd7a5-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bd7a5-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd7a5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bd7a5-137">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd7a5-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd7a5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd7a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd7a5-139">Berechnen einer Prüfsumme für die Datei System Erkennung</span><span class="sxs-lookup"><span data-stu-id="bd7a5-139">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="bd7a5-140">Datei System Erkennung</span><span class="sxs-lookup"><span data-stu-id="bd7a5-140">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="bd7a5-141">**Informationen zur Datei \_ System \_ Erkennung \_**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-141">**FILE\_SYSTEM\_RECOGNITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[<span data-ttu-id="bd7a5-142">**FSCTL- \_ Abfrage \_ Datei \_ System \_ Erkennung**</span><span class="sxs-lookup"><span data-stu-id="bd7a5-142">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

