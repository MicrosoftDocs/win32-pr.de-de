---
description: Bietet Zugriff auf Informationen zu einzelnen Aufrufern in einer Auflistung von Aufrufern. Die Auflistung stellt die Kette der Aufrufe dar, die mit dem aktuellen aufrufenden, und jeder Aufrufer in der Auflistung stellt die Identität eines Aufrufers dar.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: SecurityCaller-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342189"
---
# <a name="securitycallers-class"></a><span data-ttu-id="42a67-104">SecurityCaller-Klasse</span><span class="sxs-lookup"><span data-stu-id="42a67-104">SecurityCallers class</span></span>

<span data-ttu-id="42a67-105">Bietet Zugriff auf Informationen zu einzelnen Aufrufern in einer Auflistung von Aufrufern.</span><span class="sxs-lookup"><span data-stu-id="42a67-105">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="42a67-106">Die Auflistung stellt die Kette der Aufrufe dar, die mit dem aktuellen aufrufenden, und jeder Aufrufer in der Auflistung stellt die Identität eines Aufrufers dar.</span><span class="sxs-lookup"><span data-stu-id="42a67-106">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> <span data-ttu-id="42a67-107">Nur Aufrufer, die eine Grenze überschreiten, in der die Sicherheit geprüft wird, sind in der Kette der Aufru</span><span class="sxs-lookup"><span data-stu-id="42a67-107">Only callers who cross a boundary where security is checked are included in the chain of callers.</span></span> <span data-ttu-id="42a67-108">(In der com+-Umgebung wird die Sicherheit an den Anwendungsgrenzen geprüft.) Der Zugriff auf Informationen über die Identität eines bestimmten Aufrufers wird über die [**SecurityIdentity**](securityidentity.md) -Klasse, eine Identitäts Sammlung, bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="42a67-108">(In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through the [**SecurityIdentity**](securityidentity.md) class, an identity collection.</span></span>

<span data-ttu-id="42a67-109">Nur com+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityCaller** -Klasse zugreifen.</span><span class="sxs-lookup"><span data-stu-id="42a67-109">Only COM+ applications that use role-based security can access the **SecurityCallers** class.</span></span> <span data-ttu-id="42a67-110">Weitere Informationen zu Rollen finden Sie unter Rollen [basierte Sicherheitsverwaltung](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="42a67-110">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="42a67-111">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="42a67-111">When to implement</span></span>

<span data-ttu-id="42a67-112">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="42a67-112">This class is implemented by COM+.</span></span>



| <span data-ttu-id="42a67-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a67-113">Requirement</span></span> | <span data-ttu-id="42a67-114">Wert</span><span class="sxs-lookup"><span data-stu-id="42a67-114">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="42a67-115">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="42a67-115">Interfaces</span></span> | [<span data-ttu-id="42a67-116">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="42a67-116">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="42a67-117">Verwendung</span><span class="sxs-lookup"><span data-stu-id="42a67-117">When to use</span></span>

<span data-ttu-id="42a67-118">Verwenden Sie diese Klasse, um auf die Methoden von [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="42a67-118">Use this class to access the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="42a67-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a67-119">Remarks</span></span>

<span data-ttu-id="42a67-120">Ein **SecurityCaller** -Objekt kann nicht direkt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="42a67-120">You cannot directly create a **SecurityCallers** object.</span></span> <span data-ttu-id="42a67-121">Um die Methoden von [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)verwenden zu können, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID \_ ISecurityCallContext für den *riid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="42a67-121">To use the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="42a67-122">Rufen Sie als nächstes [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) auf, um ein Kontext Element für den Sicherheits Aufruf anzufordern, das eine Sammlung von Sicherheits Identitäten ist (z. b. "DirectCaller" oder "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="42a67-122">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

<span data-ttu-id="42a67-123">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="42a67-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="42a67-124">Ein SecurityCaller-Objekt kann nicht direkt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="42a67-124">You cannot directly create a SecurityCallers object.</span></span> <span data-ttu-id="42a67-125">Um die zugehörigen Eigenschaften verwenden zu können, müssen Sie mithilfe von [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)eine referenzce zu ihrer Implementierung abrufen.</span><span class="sxs-lookup"><span data-stu-id="42a67-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="42a67-126">Anschließend erhalten Sie die Item-Eigenschaft des-Objekts, das ein Kontext Element für den Sicherheits Aufruf anfordert, bei dem es sich um eine Sammlung von Sicherheits Identitäten handelt (z.b. "DirectCaller" oder "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="42a67-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

## <a name="requirements"></a><span data-ttu-id="42a67-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42a67-127">Requirements</span></span>



| <span data-ttu-id="42a67-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a67-128">Requirement</span></span> | <span data-ttu-id="42a67-129">Wert</span><span class="sxs-lookup"><span data-stu-id="42a67-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42a67-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42a67-130">Minimum supported client</span></span><br/> | <span data-ttu-id="42a67-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42a67-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="42a67-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42a67-132">Minimum supported server</span></span><br/> | <span data-ttu-id="42a67-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42a67-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42a67-134">Header</span><span class="sxs-lookup"><span data-stu-id="42a67-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a67-135"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="42a67-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a67-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42a67-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a67-137">**Getsecuritycallcontext**</span><span class="sxs-lookup"><span data-stu-id="42a67-137">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="42a67-138">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="42a67-138">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="42a67-139">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="42a67-139">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="42a67-140">Rollenbasierte Sicherheitsverwaltung</span><span class="sxs-lookup"><span data-stu-id="42a67-140">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="42a67-141">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="42a67-141">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="42a67-142">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="42a67-142">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

