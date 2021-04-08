---
description: Bietet Zugriff auf eine Auflistung von Sicherheitsinformationen, die die Identität eines Aufrufers darstellen. Mit dieser Klasse können Sie einen bestimmten Aufrufer in einer Kette von Aufrufern ermitteln, die Teil des Sicherheits Aufruf Kontexts ist.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: SecurityIdentity-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761556"
---
# <a name="securityidentity-class"></a><span data-ttu-id="7aedd-104">SecurityIdentity-Klasse</span><span class="sxs-lookup"><span data-stu-id="7aedd-104">SecurityIdentity class</span></span>

<span data-ttu-id="7aedd-105">Bietet Zugriff auf eine Auflistung von Sicherheitsinformationen, die die Identität eines Aufrufers darstellen.</span><span class="sxs-lookup"><span data-stu-id="7aedd-105">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="7aedd-106">Mit dieser Klasse können Sie einen bestimmten Aufrufer in einer Kette von Aufrufern ermitteln, die Teil des Sicherheits Aufruf Kontexts ist.</span><span class="sxs-lookup"><span data-stu-id="7aedd-106">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span> <span data-ttu-id="7aedd-107">Weitere Informationen zum Zugriff auf die Kontextinformationen von Sicherheits aufrufen finden Sie Unterprogramm gesteuerte Komponentensicherheit.</span><span class="sxs-lookup"><span data-stu-id="7aedd-107">For more information about how security call context information is accessed, see Programmatic Component Security.</span></span>

<span data-ttu-id="7aedd-108">Nur com+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityIdentity** -Klasse zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7aedd-108">Only COM+ applications that use role-based security can access the **SecurityIdentity** class.</span></span> <span data-ttu-id="7aedd-109">Weitere Informationen zu Rollen finden Sie unter Rollen [basierte Sicherheitsverwaltung](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="7aedd-109">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="7aedd-110">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="7aedd-110">When to implement</span></span>

<span data-ttu-id="7aedd-111">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="7aedd-111">This class is implemented by COM+.</span></span>



| <span data-ttu-id="7aedd-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aedd-112">Requirement</span></span> | <span data-ttu-id="7aedd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7aedd-113">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="7aedd-114">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7aedd-114">Interfaces</span></span> | [<span data-ttu-id="7aedd-115">**Isecurityidentitycoll**</span><span class="sxs-lookup"><span data-stu-id="7aedd-115">**ISecurityIdentityColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="7aedd-116">Verwendung</span><span class="sxs-lookup"><span data-stu-id="7aedd-116">When to use</span></span>

<span data-ttu-id="7aedd-117">Verwenden Sie diese Klasse, um auf die Methoden von [**isecurityidentitycoll**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7aedd-117">Use this class to access the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="7aedd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aedd-118">Remarks</span></span>

<span data-ttu-id="7aedd-119">Sie können ein **SecurityIdentity** -Objekt nicht direkt erstellen.</span><span class="sxs-lookup"><span data-stu-id="7aedd-119">You cannot directly create a **SecurityIdentity** object.</span></span> <span data-ttu-id="7aedd-120">Um die Methoden von [**isecurityidentitycoll**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)verwenden zu können, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID \_ ISecurityCallContext für den *riid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7aedd-120">To use the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="7aedd-121">Rufen Sie als nächstes [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) auf, um ein Kontext Element für den Sicherheits Aufruf anzufordern, das eine Sammlung von Sicherheits Identitäten ist (z. b. "DirectCaller" oder "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="7aedd-121">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="7aedd-122">Rufen Sie dann [**isecurityidentitycoll:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) auf, um ein Sicherheits Identitätselement abzurufen (z. b. "Name" oder "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="7aedd-122">Then call [**ISecurityIdentityColl::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

<span data-ttu-id="7aedd-123">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="7aedd-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="7aedd-124">Sie können ein SecurityIdentity-Objekt nicht direkt erstellen.</span><span class="sxs-lookup"><span data-stu-id="7aedd-124">You cannot directly create a SecurityIdentity object.</span></span> <span data-ttu-id="7aedd-125">Um die zugehörigen Eigenschaften verwenden zu können, müssen Sie mithilfe von [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)eine referenzce zu ihrer Implementierung abrufen.</span><span class="sxs-lookup"><span data-stu-id="7aedd-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="7aedd-126">Anschließend erhalten Sie die Item-Eigenschaft des-Objekts, das ein Kontext Element für den Sicherheits Aufruf anfordert, bei dem es sich um eine Sammlung von Sicherheits Identitäten handelt (z.b. "DirectCaller" oder "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="7aedd-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="7aedd-127">Verwenden Sie dann die Item-Eigenschaft des SecurityIdentity-Objekts, um ein Sicherheits Identitätselement abzurufen (z. b. "Name" oder "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="7aedd-127">Then, use the Item property of the SecurityIdentity object to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

## <a name="requirements"></a><span data-ttu-id="7aedd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aedd-128">Requirements</span></span>



| <span data-ttu-id="7aedd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aedd-129">Requirement</span></span> | <span data-ttu-id="7aedd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7aedd-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7aedd-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7aedd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7aedd-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7aedd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7aedd-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7aedd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7aedd-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7aedd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7aedd-135">Header</span><span class="sxs-lookup"><span data-stu-id="7aedd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aedd-136"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7aedd-136"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aedd-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aedd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aedd-138">**Getsecuritycallcontext**</span><span class="sxs-lookup"><span data-stu-id="7aedd-138">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="7aedd-139">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="7aedd-139">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="7aedd-140">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="7aedd-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="7aedd-141">Rollenbasierte Sicherheitsverwaltung</span><span class="sxs-lookup"><span data-stu-id="7aedd-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="7aedd-142">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="7aedd-142">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="7aedd-143">**SecurityCaller**</span><span class="sxs-lookup"><span data-stu-id="7aedd-143">**SecurityCallers**</span></span>](securitycallers.md)
</dt> </dl>

 

