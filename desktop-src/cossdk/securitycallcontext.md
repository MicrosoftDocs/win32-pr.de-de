---
description: Bietet Zugriff auf den Sicherheitskontext des aktuellen Aufrufer, der Informationen zu den Aufrufern eines Objekts enthält.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: SecurityCallContext-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366385"
---
# <a name="securitycallcontext-class"></a><span data-ttu-id="6520a-103">SecurityCallContext-Klasse</span><span class="sxs-lookup"><span data-stu-id="6520a-103">SecurityCallContext class</span></span>

<span data-ttu-id="6520a-104">Bietet Zugriff auf den Sicherheitskontext des aktuellen Aufrufer, der Informationen zu den Aufrufern eines Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="6520a-104">Provides access to the current call's security context, which contains information about an object's callers.</span></span> <span data-ttu-id="6520a-105">Mit dieser Klasse können Sie auch feststellen, ob der direkte Aufrufer eines Objekts ein Member einer bestimmten Rolle ist und ob die Sicherheit für das Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6520a-105">Using this class, you can also find out whether an object's direct caller is a member of a particular role and whether security is enabled for the object.</span></span>

<span data-ttu-id="6520a-106">Nur com+-Anwendungen, die rollenbasierte Sicherheit verwenden, können auf die **SecurityCallContext** -Klasse zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6520a-106">Only COM+ applications that use role-based security can access the **SecurityCallContext** class.</span></span> <span data-ttu-id="6520a-107">Weitere Informationen zu Rollen finden Sie unter Rollen [basierte Sicherheitsverwaltung](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="6520a-107">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="6520a-108">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="6520a-108">When to implement</span></span>

<span data-ttu-id="6520a-109">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="6520a-109">This class is implemented by COM+.</span></span>



| <span data-ttu-id="6520a-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6520a-110">Requirement</span></span> | <span data-ttu-id="6520a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="6520a-111">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="6520a-112">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6520a-112">Interfaces</span></span> | [<span data-ttu-id="6520a-113">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="6520a-113">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="6520a-114">Verwendung</span><span class="sxs-lookup"><span data-stu-id="6520a-114">When to use</span></span>

<span data-ttu-id="6520a-115">Verwenden Sie diese Klasse, um auf die Methoden von [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6520a-115">Use this class to access the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="remarks"></a><span data-ttu-id="6520a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6520a-116">Remarks</span></span>

<span data-ttu-id="6520a-117">Sie können ein **SecurityCallContext** -Objekt nicht direkt erstellen.</span><span class="sxs-lookup"><span data-stu-id="6520a-117">You cannot directly create a **SecurityCallContext** object.</span></span> <span data-ttu-id="6520a-118">Um die Methoden von [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)verwenden zu können, müssen Sie einen Verweis auf seine Implementierung abrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)aufrufen und IID \_ ISecurityCallContext für den *riid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6520a-118">To use the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span>

<span data-ttu-id="6520a-119">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="6520a-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="6520a-120">Ein SecurityCallContext-Objekt kann mithilfe von "COMSVCSLIB. SecurityCallContext" als Klassenname deklariert werden. Sie wird erstellt, indem [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6520a-120">A SecurityCallContext object can be declared using "COMSVCSLib.SecurityCallContext" as the class name; it is created by calling [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="6520a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6520a-121">Requirements</span></span>



| <span data-ttu-id="6520a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6520a-122">Requirement</span></span> | <span data-ttu-id="6520a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6520a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6520a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6520a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6520a-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6520a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6520a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6520a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6520a-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6520a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6520a-128">Header</span><span class="sxs-lookup"><span data-stu-id="6520a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6520a-129"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6520a-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6520a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6520a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6520a-131">**Getsecuritycallcontext**</span><span class="sxs-lookup"><span data-stu-id="6520a-131">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="6520a-132">**ISecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="6520a-132">**ISecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="6520a-133">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="6520a-133">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="6520a-134">Rollenbasierte Sicherheitsverwaltung</span><span class="sxs-lookup"><span data-stu-id="6520a-134">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="6520a-135">**SecurityCaller**</span><span class="sxs-lookup"><span data-stu-id="6520a-135">**SecurityCallers**</span></span>](securitycallers.md)
</dt> <dt>

[<span data-ttu-id="6520a-136">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="6520a-136">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

