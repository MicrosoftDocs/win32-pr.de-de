---
description: Bestimmen, ob Role-Based Sicherheit aktiviert ist
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Bestimmen, ob Role-Based Sicherheit aktiviert ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127552"
---
# <a name="determining-whether-role-based-security-is-enabled"></a><span data-ttu-id="587ef-103">Bestimmen, ob Role-Based Sicherheit aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="587ef-103">Determining Whether Role-Based Security Is Enabled</span></span>

<span data-ttu-id="587ef-104">Mithilfe der [**ISecurityCallContext:: issecurityaktivierten**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) -Methode, die im Kontext Objekt für den Sicherheits Aufruf verfügbar ist, können Sie bestimmen, ob die Sicherheit für das aktuelle Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="587ef-104">By using the [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) method available from the security call context object, you can determine whether security is enabled for the current object.</span></span> <span data-ttu-id="587ef-105">Sie sollten " **issecurityaktivierte** " aufrufen, bevor Sie ISecurityCallContext::[**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) zum Überprüfen der Rollen Mitgliedschaft verwenden, weil **isCallerInRole** true zurückgibt, wenn die Sicherheit nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="587ef-105">You should call **IsSecurityEnabled** before you use ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to check role membership because **IsCallerInRole** returns True if security is not enabled.</span></span>

<span data-ttu-id="587ef-106">Microsoft Visual Basic-Entwickler rufen [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) auf, um einen Verweis auf ein [**SecurityCallContext**](securitycallcontext.md) -Objekt zu erhalten, und rufen dann [**issecurityaktivierte**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled)auf, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="587ef-106">Microsoft Visual Basic developers call [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) to obtain a reference to a [**SecurityCallContext**](securitycallcontext.md) object and then call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), as shown in the following example:</span></span>


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



<span data-ttu-id="587ef-107">Microsoft Visual C++ Entwickler können [**ISecurityCallContext:: issecurityaktiviert**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) aufrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) aufrufen, um einen Zeiger auf [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) zu erhalten und dann **issecurityaktivierte** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="587ef-107">Microsoft Visual C++ developers can call [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) and then calling **IsSecurityEnabled**.</span></span> <span data-ttu-id="587ef-108">Es folgt ein kurzes Beispiel:</span><span class="sxs-lookup"><span data-stu-id="587ef-108">A brief example follows:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsEnabled;

HRESULT hr1 = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr1)) throw(hr1);
if (NULL == pSecCtx) {
    // Display error message.
    return E_FAIL;
}

HRESULT hr2 = pSecCtx->IsSecurityEnabled(&bIsEnabled);
return hr2;
```



<span data-ttu-id="587ef-109">Obwohl die bevorzugte Methode zum aufzurufen von [**issecurityaktiviist**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) , das Kontext Objekt für den Sicherheits Rückruf verwendet wird, können Sie **issecurityaktivierte** auch über den Objekt Kontext aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="587ef-109">Although the preferred way to call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) is by using the security call context object, you can also call **IsSecurityEnabled** through the object context.</span></span> <span data-ttu-id="587ef-110">(Weitere Informationen finden Sie unter [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) oder [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)</span><span class="sxs-lookup"><span data-stu-id="587ef-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="587ef-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="587ef-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="587ef-112">Aufrufen von Kontextinformationen für den Sicherheitskontext</span><span class="sxs-lookup"><span data-stu-id="587ef-112">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="587ef-113">Überprüfen der Rollen Mitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="587ef-113">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="587ef-114">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="587ef-114">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
