---
description: Ruft einen booleschen Wert ab, der angibt, ob die Kontingent Datei für das Volume gerade neu erstellt wird.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Diskquotacontrol. quotafilerebuilding (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977504"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a><span data-ttu-id="038b5-103">Diskquotacontrol. quotafilerebuilding (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="038b5-103">DiskQuotaControl.QuotaFileRebuilding property</span></span>

<span data-ttu-id="038b5-104">Ruft einen booleschen Wert ab, der angibt, ob die Kontingent Datei für das Volume gerade neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="038b5-104">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span>

<span data-ttu-id="038b5-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="038b5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="038b5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="038b5-106">Syntax</span></span>


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a><span data-ttu-id="038b5-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="038b5-107">Property value</span></span>

<span data-ttu-id="038b5-108">Diese Eigenschaft wird auf **true** festgelegt, wenn die Kontingent Datei neu erstellt wird, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="038b5-108">This property is set to **TRUE** if the quota file is being rebuilt, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="038b5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="038b5-109">Remarks</span></span>

<span data-ttu-id="038b5-110">Die Kontingent Datei wird automatisch neu erstellt, wenn Kontingente auf dem System aktiviert sind oder wenn mindestens ein Benutzereintrag zum Löschen markiert ist.</span><span class="sxs-lookup"><span data-stu-id="038b5-110">The quota file is automatically rebuilt when quotas are enabled on the system or when one or more user entries are marked for deletion.</span></span>

## <a name="requirements"></a><span data-ttu-id="038b5-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="038b5-111">Requirements</span></span>



| <span data-ttu-id="038b5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="038b5-112">Requirement</span></span> | <span data-ttu-id="038b5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="038b5-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038b5-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="038b5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="038b5-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="038b5-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="038b5-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="038b5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="038b5-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="038b5-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="038b5-118">DLL</span><span class="sxs-lookup"><span data-stu-id="038b5-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="038b5-119"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="038b5-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="038b5-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="038b5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038b5-121">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="038b5-121">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




