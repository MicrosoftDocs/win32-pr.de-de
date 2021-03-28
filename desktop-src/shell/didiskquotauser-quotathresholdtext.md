---
description: Ruft den Warnungs Schwellenwert des Benutzers als Text Zeichenfolge ab.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: Didiskquotauser. quotader OLDTEXT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977217"
---
# <a name="didiskquotauserquotathresholdtext-property"></a><span data-ttu-id="aef0b-103">Didiskquotauser. quotader OLDTEXT-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aef0b-103">DIDiskQuotaUser.QuotaThresholdText property</span></span>

<span data-ttu-id="aef0b-104">Ruft den Warnungs Schwellenwert des Benutzers als Text Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="aef0b-104">Gets the user's warning threshold as a text string.</span></span>

<span data-ttu-id="aef0b-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="aef0b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef0b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="aef0b-106">Syntax</span></span>


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="aef0b-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="aef0b-107">Property value</span></span>

<span data-ttu-id="aef0b-108">Der Zeichen folgen Wert, der den Warnungs Schwellenwert des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="aef0b-108">The string value that contains the user's warning threshold.</span></span> <span data-ttu-id="aef0b-109">Wenn die Datenträger Nutzung eines Benutzers diesen Wert überschreitet und die [**logquotathreshold**](diskquotacontrol-logquotathreshold.md) -Eigenschaft auf **true** festgelegt ist, generiert das System einen Ereignisprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="aef0b-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef0b-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aef0b-110">Requirements</span></span>



| <span data-ttu-id="aef0b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aef0b-111">Requirement</span></span> | <span data-ttu-id="aef0b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="aef0b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef0b-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aef0b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="aef0b-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aef0b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aef0b-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aef0b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="aef0b-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aef0b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="aef0b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="aef0b-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef0b-118"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="aef0b-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef0b-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aef0b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef0b-120">**Idiskquotauser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="aef0b-120">**IDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="aef0b-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="aef0b-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="aef0b-122">**Quotalimittext**</span><span class="sxs-lookup"><span data-stu-id="aef0b-122">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="aef0b-123">**Quotathreshold**</span><span class="sxs-lookup"><span data-stu-id="aef0b-123">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




