---
description: Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmeldeinformationen dynamisch zur Laufzeit angeben können, um nicht in die Domäne beigetretene Container mit Active Directory zu authentifizieren.
title: ICcgDomainAuthCredentials-Schnittstelle (ccgplugins.h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387805"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="1f53d-103">ICcgDomainAuthCredentials-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1f53d-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="1f53d-104">Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmeldeinformationen dynamisch zur Laufzeit angeben können, um nicht in die Domäne beigetretene Container mit Active Directory zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="1f53d-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="1f53d-105">Member</span><span class="sxs-lookup"><span data-stu-id="1f53d-105">Members</span></span>

<span data-ttu-id="1f53d-106">Die **ICcgDomainAuthCredentials-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="1f53d-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1f53d-107">**ICcgDomainAuthCredentials** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="1f53d-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="1f53d-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1f53d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1f53d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1f53d-109">Methods</span></span>

<span data-ttu-id="1f53d-110">Die **ICcgDomainAuthCredentials-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1f53d-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="1f53d-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1f53d-111">Method</span></span>                                           | <span data-ttu-id="1f53d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f53d-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f53d-113">**GetPasswordCredentials**</span><span class="sxs-lookup"><span data-stu-id="1f53d-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="1f53d-114">Gibt Anmeldeinformationen zurück, um einen nicht in die Domäne beigetretenen Container bei Active Directory zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="1f53d-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="1f53d-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1f53d-115">Requirements</span></span>



| <span data-ttu-id="1f53d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f53d-116">Requirement</span></span> | <span data-ttu-id="1f53d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1f53d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f53d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f53d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f53d-119">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f53d-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f53d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f53d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f53d-121">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f53d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f53d-122">Header</span><span class="sxs-lookup"><span data-stu-id="1f53d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f53d-123"><dt>ccgplugins.h</dt></span><span class="sxs-lookup"><span data-stu-id="1f53d-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f53d-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1f53d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f53d-125"><dt>ccgplugins.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f53d-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1f53d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1f53d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f53d-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f53d-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f53d-128">IID</span><span class="sxs-lookup"><span data-stu-id="1f53d-128">IID</span></span><br/>                      | <span data-ttu-id="1f53d-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="1f53d-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

