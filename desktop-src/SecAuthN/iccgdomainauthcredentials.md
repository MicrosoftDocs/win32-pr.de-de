---
description: Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmelde Informationen zur Laufzeit dynamisch bereitstellen können, um nicht mit der Domäne verbundene Container mit Active Directory zu authentifizieren.
title: Iccgdomainauth-Anmelde Informationen-Schnittstelle (ccgplugins. h)
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
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106366564"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="62ffd-103">Iccgdomainauth-Anmelde Informationen (Schnittstelle)</span><span class="sxs-lookup"><span data-stu-id="62ffd-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="62ffd-104">Eine vom Client implementierte Schnittstelle, mit der Entwickler ihre eigenen Anmelde Informationen zur Laufzeit dynamisch bereitstellen können, um nicht mit der Domäne verbundene Container mit Active Directory zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="62ffd-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="62ffd-105">Member</span><span class="sxs-lookup"><span data-stu-id="62ffd-105">Members</span></span>

<span data-ttu-id="62ffd-106">Die **iccgdomainauthanmelde** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="62ffd-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="62ffd-107">**Iccgdomainauthanmeldeinformationen** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="62ffd-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="62ffd-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="62ffd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62ffd-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="62ffd-109">Methods</span></span>

<span data-ttu-id="62ffd-110">Die **iccgdomainauthanmelde** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="62ffd-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="62ffd-111">Methode</span><span class="sxs-lookup"><span data-stu-id="62ffd-111">Method</span></span>                                           | <span data-ttu-id="62ffd-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62ffd-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62ffd-113">**Getpasswordanmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="62ffd-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="62ffd-114">Gibt Anmelde Informationen zurück, um einen nicht in die Domäne eingebundenen Container mit Active Directory zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="62ffd-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="62ffd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62ffd-115">Requirements</span></span>



| <span data-ttu-id="62ffd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62ffd-116">Requirement</span></span> | <span data-ttu-id="62ffd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="62ffd-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62ffd-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62ffd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="62ffd-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62ffd-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="62ffd-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62ffd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="62ffd-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62ffd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62ffd-122">Header</span><span class="sxs-lookup"><span data-stu-id="62ffd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ffd-123"><dt>ccgplugins. h</dt></span><span class="sxs-lookup"><span data-stu-id="62ffd-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="62ffd-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="62ffd-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="62ffd-125"><dt>ccgplugins. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="62ffd-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="62ffd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="62ffd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ffd-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ffd-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="62ffd-128">IID</span><span class="sxs-lookup"><span data-stu-id="62ffd-128">IID</span></span><br/>                      | <span data-ttu-id="62ffd-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="62ffd-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

