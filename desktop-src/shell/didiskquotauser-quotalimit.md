---
description: Legt das aktuelle Kontingentlimit des Benutzers fest oder ruft es ab.
title: DIDiskQuotaUser.QuotaLimit (Eigenschaft)
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
ms.openlocfilehash: b1971871bdeb18e3c7dd4c7978152bbec276fa8b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841631"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="da77c-103">DIDiskQuotaUser.QuotaLimit (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="da77c-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="da77c-104">Legt die aktuelle Kontingentgrenze des Benutzers fest oder [**ruft sie ab.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="da77c-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="da77c-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="da77c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="da77c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="da77c-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="da77c-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="da77c-107">Property value</span></span>

<span data-ttu-id="da77c-108">Ein **Ganzzahlwert,** der die aktuelle Kontingentgrenze des Benutzers in Bytes angibt oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="da77c-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="da77c-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da77c-109">Requirements</span></span>



| <span data-ttu-id="da77c-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da77c-110">Requirement</span></span> | <span data-ttu-id="da77c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="da77c-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da77c-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da77c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="da77c-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da77c-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da77c-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da77c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="da77c-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da77c-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="da77c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="da77c-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da77c-117"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="da77c-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da77c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da77c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da77c-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="da77c-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="da77c-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="da77c-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="da77c-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="da77c-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




