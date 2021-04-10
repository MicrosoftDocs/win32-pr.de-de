---
description: Enthält das Standard Informations Attribut. Dieses Attribut ist in jedem Basisdatei Daten Satz vorhanden und muss ansässig sein.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: STANDARD_INFORMATION Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041321"
---
# <a name="standard_information-structure"></a><span data-ttu-id="c01a6-104">Standard \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="c01a6-104">STANDARD\_INFORMATION structure</span></span>

<span data-ttu-id="c01a6-105">\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]</span><span class="sxs-lookup"><span data-stu-id="c01a6-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="c01a6-106">Enthält das Standard Informations Attribut.</span><span class="sxs-lookup"><span data-stu-id="c01a6-106">Contains the standard information attribute.</span></span> <span data-ttu-id="c01a6-107">Dieses Attribut ist in jedem Basisdatei Daten Satz vorhanden und muss ansässig sein.</span><span class="sxs-lookup"><span data-stu-id="c01a6-107">This attribute is present in every base file record and must be resident.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c01a6-108">Syntax</span></span>


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="c01a6-109">Member</span><span class="sxs-lookup"><span data-stu-id="c01a6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c01a6-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c01a6-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c01a6-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c01a6-111">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c01a6-112">**OwnerID**</span><span class="sxs-lookup"><span data-stu-id="c01a6-112">**OwnerId**</span></span>
</dt> <dd>

<span data-ttu-id="c01a6-113">Der Bezeichner des Datei Besitzers aus dem Sicherheitsindex.</span><span class="sxs-lookup"><span data-stu-id="c01a6-113">The identifier of the file owner, from the security index.</span></span>

</dd> <dt>

<span data-ttu-id="c01a6-114">**Securityid**</span><span class="sxs-lookup"><span data-stu-id="c01a6-114">**SecurityId**</span></span>
</dt> <dd>

<span data-ttu-id="c01a6-115">Die Sicherheits-ID für die Datei.</span><span class="sxs-lookup"><span data-stu-id="c01a6-115">The security identifier for the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c01a6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c01a6-116">Remarks</span></span>

<span data-ttu-id="c01a6-117">Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.</span><span class="sxs-lookup"><span data-stu-id="c01a6-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="c01a6-118">Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.</span><span class="sxs-lookup"><span data-stu-id="c01a6-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="c01a6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c01a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01a6-120">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="c01a6-120">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
