---
description: Ruft den Namen des Konto Containers des Benutzers ab.
title: Didiskquotauser. accountcontainername-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750225"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="1cc23-103">Didiskquotauser. accountcontainername-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1cc23-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="1cc23-104">Ruft den Namen des Konto Containers des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="1cc23-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="1cc23-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1cc23-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc23-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cc23-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="1cc23-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1cc23-107">Property value</span></span>

<span data-ttu-id="1cc23-108">Ein Zeichen folgen Wert, der auf den Konto Container Namen des Benutzers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1cc23-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc23-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cc23-109">Remarks</span></span>

<span data-ttu-id="1cc23-110">Für Konten ohne Informationen zu Verzeichnisdiensten enthält diese Eigenschaft den Domänen Namen.</span><span class="sxs-lookup"><span data-stu-id="1cc23-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="1cc23-111">Bei Konten mit Verzeichnisdienst Informationen enthält diese Eigenschaft einen kanonischen Namen, bei dem der abschließende Objektname entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="1cc23-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc23-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1cc23-112">Requirements</span></span>



| <span data-ttu-id="1cc23-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cc23-113">Requirement</span></span> | <span data-ttu-id="1cc23-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1cc23-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc23-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1cc23-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc23-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1cc23-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1cc23-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1cc23-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc23-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1cc23-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1cc23-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1cc23-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cc23-120"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc23-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc23-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1cc23-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc23-122">**Didiskquotauser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1cc23-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




