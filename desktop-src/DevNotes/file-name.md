---
description: Stellt ein Dateiname-Attribut dar. Eine Datei verfügt über ein Dateiname-Attribut für jedes Verzeichnis, in das Sie eingegeben wird.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: File_name Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041329"
---
# <a name="file_name-structure"></a><span data-ttu-id="04ea9-104">Datei \_ Namen Struktur</span><span class="sxs-lookup"><span data-stu-id="04ea9-104">FILE\_NAME structure</span></span>

<span data-ttu-id="04ea9-105">\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]</span><span class="sxs-lookup"><span data-stu-id="04ea9-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="04ea9-106">Stellt ein Dateiname-Attribut dar.</span><span class="sxs-lookup"><span data-stu-id="04ea9-106">Represents a file name attribute.</span></span> <span data-ttu-id="04ea9-107">Eine Datei verfügt über ein Dateiname-Attribut für jedes Verzeichnis, in das Sie eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="04ea9-107">A file has one file name attribute for every directory it is entered into.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ea9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="04ea9-108">Syntax</span></span>


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a><span data-ttu-id="04ea9-109">Member</span><span class="sxs-lookup"><span data-stu-id="04ea9-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="04ea9-110">**"Element Verzeichnis"**</span><span class="sxs-lookup"><span data-stu-id="04ea9-110">**ParentDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="04ea9-111">Ein Datei Verweis auf das Verzeichnis, das diesen Namen indiziert.</span><span class="sxs-lookup"><span data-stu-id="04ea9-111">A file reference to the directory that indexes to this name.</span></span> <span data-ttu-id="04ea9-112">Siehe [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="04ea9-112">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ea9-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="04ea9-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="04ea9-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="04ea9-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="04ea9-115">**Datamelength**</span><span class="sxs-lookup"><span data-stu-id="04ea9-115">**FileNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="04ea9-116">Die Länge des Datei namens in Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="04ea9-116">The length of the file name, in Unicode characters.</span></span>

</dd> <dt>

<span data-ttu-id="04ea9-117">**Flags**</span><span class="sxs-lookup"><span data-stu-id="04ea9-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="04ea9-118">Die Dateiname-Flags.</span><span class="sxs-lookup"><span data-stu-id="04ea9-118">The file name flags.</span></span>

<dl> <dt>

<span data-ttu-id="04ea9-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Datei \_ Name \_ NTFS** (0x01)</span><span class="sxs-lookup"><span data-stu-id="04ea9-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE\_NAME\_NTFS** (0x01)</span></span>
</dt> <dt>

<span data-ttu-id="04ea9-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Datei \_ Name \_ DOS** (0x02)</span><span class="sxs-lookup"><span data-stu-id="04ea9-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE\_NAME\_DOS** (0x02)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="04ea9-121">**FileName**</span><span class="sxs-lookup"><span data-stu-id="04ea9-121">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="04ea9-122">Das erste Zeichen des Datei namens.</span><span class="sxs-lookup"><span data-stu-id="04ea9-122">The first character of the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04ea9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04ea9-123">Remarks</span></span>

<span data-ttu-id="04ea9-124">Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.</span><span class="sxs-lookup"><span data-stu-id="04ea9-124">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="04ea9-125">Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.</span><span class="sxs-lookup"><span data-stu-id="04ea9-125">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="04ea9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04ea9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ea9-127">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="04ea9-127">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
