---
description: Ruft die aktuelle Datenträger Verwendung des Benutzers in Bytes ab.
title: Didiskquotauser. quotaused (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128448"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="7ade5-103">Didiskquotauser. quotaused (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7ade5-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="7ade5-104">Ruft die aktuelle Datenträger Verwendung des Benutzers in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="7ade5-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="7ade5-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7ade5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ade5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ade5-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="7ade5-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7ade5-107">Property value</span></span>

<span data-ttu-id="7ade5-108">Der **ganzzahlige** Wert, der auf den derzeit verwendeten Speicherplatz festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7ade5-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="7ade5-109">Wenn die NTFS-Dateikomprimierung aktiviert ist, gibt **quotaused** die Menge an Speicherplatz an, die die Daten in einem unkomprimierten Zustand erfordern.</span><span class="sxs-lookup"><span data-stu-id="7ade5-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ade5-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7ade5-110">Requirements</span></span>



| <span data-ttu-id="7ade5-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ade5-111">Requirement</span></span> | <span data-ttu-id="7ade5-112">Wert</span><span class="sxs-lookup"><span data-stu-id="7ade5-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ade5-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ade5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7ade5-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ade5-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ade5-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ade5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7ade5-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ade5-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7ade5-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7ade5-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ade5-118"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7ade5-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ade5-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ade5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ade5-120">**Didiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="7ade5-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="7ade5-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="7ade5-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="7ade5-122">**Quotathreshold**</span><span class="sxs-lookup"><span data-stu-id="7ade5-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="7ade5-123">**Quotausedtext**</span><span class="sxs-lookup"><span data-stu-id="7ade5-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




