---
description: Überprüfen der Rollen Mitgliedschaft
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: Überprüfen der Rollen Mitgliedschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748672"
---
# <a name="checking-role-membership"></a><span data-ttu-id="c03ba-103">Überprüfen der Rollen Mitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="c03ba-103">Checking Role Membership</span></span>

<span data-ttu-id="c03ba-104">Sie können die [**ISecurityCallContext:: isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) -Methode aufrufen, um zu bestimmen, ob der direkte Aufrufer eines Objekts ein Member einer bestimmten Rolle ist.</span><span class="sxs-lookup"><span data-stu-id="c03ba-104">You can call the [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) method to determine whether an object's direct caller is a member of a particular role.</span></span> <span data-ttu-id="c03ba-105">Diese Funktion ist nützlich, wenn Sie sicherstellen möchten, dass ein bestimmter Codeblock nicht ausgeführt wird, wenn der Aufrufer nicht Mitglied einer bestimmten Rolle ist.</span><span class="sxs-lookup"><span data-stu-id="c03ba-105">This functionality is useful when you want to ensure that a certain block of code is not executed unless the caller is a member of a particular role.</span></span>

<span data-ttu-id="c03ba-106">Beispielsweise können Sie mit [**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) sicherstellen, dass Transaktionen über einen angegebenen Betrag, z. b. $1000, nur von Mitgliedern einer Manager-Rolle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c03ba-106">For example, you could use [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to ensure that transactions over a specified amount, such as $1000, are performed only by members of a Managers role.</span></span> <span data-ttu-id="c03ba-107">Wenn der Aufrufer kein Manager und die Transaktion über $1000 ist, wird die Transaktion nicht ausgeführt, und es wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c03ba-107">If the caller is not a Manager and the transaction is over $1000, the transaction is not performed and an error message is displayed.</span></span>

<span data-ttu-id="c03ba-108">Die bevorzugte Methode für den Zugriff auf [**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) erfolgt über das Kontext Objekt für den Sicherheits Aufruf, da Sie denselben Verweis auf das Kontext Objekt für den Sicherheits Aufruf zum Abrufen von Sicherheitseigenschaften verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c03ba-108">The preferred way to access [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) is through the security call context object because you can use the same reference to the security call context object to obtain security properties.</span></span> <span data-ttu-id="c03ba-109">Sie können jedoch auch über das **ObjectContext** -Objekt auf die **isCallerInRole**-Methode zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c03ba-109">However, you can also access the **IsCallerInRole** method from the **ObjectContext** object.</span></span> <span data-ttu-id="c03ba-110">(Weitere Informationen finden Sie unter [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) oder [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)</span><span class="sxs-lookup"><span data-stu-id="c03ba-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

<span data-ttu-id="c03ba-111">Wenn Sie Komponenten für eine Microsoft Visual Basic-Anwendung entwickeln, rufen Sie die [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) -Funktion auf, und verwenden Sie dann den Sicherheits Aufruf Kontext, um [**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)aufzurufen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="c03ba-111">If you are developing components for a Microsoft Visual Basic application, you call the [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) function and then use the security call context to call [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



<span data-ttu-id="c03ba-112">Wenn Sie eine C-oder C++-Anwendung entwickeln, rufen Sie mit [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) einen Zeiger auf die [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="c03ba-112">If you are developing a C or C++ application, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to retrieve a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface.</span></span> <span data-ttu-id="c03ba-113">Dann rufen Sie [**ISecurityCallContext:: isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)auf, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="c03ba-113">Then you call [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="c03ba-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c03ba-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c03ba-115">Aufrufen von Kontextinformationen für den Sicherheitskontext</span><span class="sxs-lookup"><span data-stu-id="c03ba-115">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="c03ba-116">Bestimmen, ob Role-Based Sicherheit aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="c03ba-116">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="c03ba-117">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="c03ba-117">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
