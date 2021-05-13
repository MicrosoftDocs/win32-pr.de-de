---
description: Ruft die aktuelle Datenträgerverwendung des Benutzers in Bytes ab.
title: DIDiskQuotaUser.QuotaUsed (Eigenschaft)
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
ms.openlocfilehash: a08d7579ad4de51fbc88b7091f2f906ace838883
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841571"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="7e091-103">DIDiskQuotaUser.QuotaUsed (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e091-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="7e091-104">Ruft die aktuelle Datenträgerverwendung des Benutzers in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="7e091-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="7e091-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7e091-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e091-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e091-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="7e091-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7e091-107">Property value</span></span>

<span data-ttu-id="7e091-108">Der  Ganzzahlwert, der auf die Menge des derzeit verwendeten Speicherplatzes festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7e091-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="7e091-109">Wenn die NTFS-Dateikomprimierung aktiviert ist, **gibt QuotaUsed** den Speicherplatz an, den die Daten in einem nicht komprimierten Zustand benötigen würden.</span><span class="sxs-lookup"><span data-stu-id="7e091-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e091-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e091-110">Requirements</span></span>



| <span data-ttu-id="7e091-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e091-111">Requirement</span></span> | <span data-ttu-id="7e091-112">Wert</span><span class="sxs-lookup"><span data-stu-id="7e091-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e091-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e091-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7e091-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e091-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e091-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e091-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7e091-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e091-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7e091-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7e091-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e091-118"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7e091-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e091-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e091-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e091-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="7e091-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="7e091-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="7e091-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="7e091-122">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="7e091-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="7e091-123">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="7e091-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




