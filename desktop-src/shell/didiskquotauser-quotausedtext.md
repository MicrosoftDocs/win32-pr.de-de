---
description: Ruft die aktuelle Datenträger Verwendung des Benutzers als Text Zeichenfolge ab.
title: Didiskquotauser. quotausedtext (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977208"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="09b6b-103">Didiskquotauser. quotausedtext (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="09b6b-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="09b6b-104">Ruft die aktuelle Datenträger Verwendung des Benutzers als Text Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="09b6b-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="09b6b-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="09b6b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b6b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="09b6b-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="09b6b-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="09b6b-107">Property value</span></span>

<span data-ttu-id="09b6b-108">Ein Zeichen folgen Wert, der auf den derzeit verwendeten Speicherplatz festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="09b6b-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="09b6b-109">Wenn die NTFS-Dateikomprimierung aktiviert ist, gibt diese Eigenschaft die Menge an Speicherplatz an, die die Daten in einem unkomprimierten Zustand erfordern.</span><span class="sxs-lookup"><span data-stu-id="09b6b-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b6b-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="09b6b-110">Requirements</span></span>



| <span data-ttu-id="09b6b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09b6b-111">Requirement</span></span> | <span data-ttu-id="09b6b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="09b6b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b6b-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09b6b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="09b6b-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09b6b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09b6b-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09b6b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="09b6b-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09b6b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="09b6b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="09b6b-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09b6b-118"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="09b6b-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b6b-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="09b6b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b6b-120">**Didiskquotauser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="09b6b-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="09b6b-121">**Quotalimittext**</span><span class="sxs-lookup"><span data-stu-id="09b6b-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="09b6b-122">**Quotader OLDTEXT**</span><span class="sxs-lookup"><span data-stu-id="09b6b-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="09b6b-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="09b6b-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




