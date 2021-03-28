---
description: Legt die aktuelle Kontingent Grenze des Benutzers fest oder ruft diese ab.
title: Didiskquotauser. quotalimit (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977224"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="4f028-103">Didiskquotauser. quotalimit (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4f028-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="4f028-104">Legt die aktuelle [**Kontingent Grenze**](diskquotacontrol-object.md)des Benutzers fest oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="4f028-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="4f028-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4f028-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f028-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f028-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="4f028-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4f028-107">Property value</span></span>

<span data-ttu-id="4f028-108">Ein **ganzzahliger** Wert, der die aktuelle Kontingent Grenze des Benutzers in Bytes angibt oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="4f028-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f028-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4f028-109">Requirements</span></span>



| <span data-ttu-id="4f028-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f028-110">Requirement</span></span> | <span data-ttu-id="4f028-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4f028-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f028-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f028-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4f028-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f028-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f028-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f028-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4f028-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f028-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4f028-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4f028-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f028-117"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4f028-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f028-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f028-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f028-119">**Defaultquotalimit**</span><span class="sxs-lookup"><span data-stu-id="4f028-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="4f028-120">**Didiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="4f028-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="4f028-121">**Quotalimittext**</span><span class="sxs-lookup"><span data-stu-id="4f028-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




