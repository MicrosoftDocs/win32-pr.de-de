---
description: Ruft den Namen des Kontocontainers des Benutzers ab.
title: DIDiskQuotaUser.AccountContainerName (Eigenschaft)
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
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843351"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="a9a04-103">DIDiskQuotaUser.AccountContainerName (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a9a04-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="a9a04-104">Ruft den Namen des Kontocontainers des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="a9a04-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="a9a04-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a9a04-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a04-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9a04-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="a9a04-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a9a04-107">Property value</span></span>

<span data-ttu-id="a9a04-108">Ein Zeichenfolgenwert, der auf den Namen des Kontocontainers des Benutzers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a9a04-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a04-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9a04-109">Remarks</span></span>

<span data-ttu-id="a9a04-110">Für Konten ohne Verzeichnisdienstinformationen enthält diese Eigenschaft den Domänennamen.</span><span class="sxs-lookup"><span data-stu-id="a9a04-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="a9a04-111">Für Konten mit Verzeichnisdienstinformationen enthält diese Eigenschaft einen kanonischen Namen, bei dem der beendende Objektname entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="a9a04-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a04-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9a04-112">Requirements</span></span>



| <span data-ttu-id="a9a04-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9a04-113">Requirement</span></span> | <span data-ttu-id="a9a04-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a9a04-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a04-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9a04-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a04-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9a04-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9a04-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9a04-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a04-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9a04-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a9a04-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a9a04-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a04-120"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a04-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a04-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9a04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a04-122">**DIDiskQuotaUser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a9a04-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




