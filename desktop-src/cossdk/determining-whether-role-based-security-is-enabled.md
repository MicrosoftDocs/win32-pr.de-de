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
# <a name="determining-whether-role-based-security-is-enabled"></a>Bestimmen, ob Role-Based Sicherheit aktiviert ist

Mithilfe der [**ISecurityCallContext:: issecurityaktivierten**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) -Methode, die im Kontext Objekt für den Sicherheits Aufruf verfügbar ist, können Sie bestimmen, ob die Sicherheit für das aktuelle Objekt aktiviert ist. Sie sollten " **issecurityaktivierte** " aufrufen, bevor Sie ISecurityCallContext::[**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) zum Überprüfen der Rollen Mitgliedschaft verwenden, weil **isCallerInRole** true zurückgibt, wenn die Sicherheit nicht aktiviert ist.

Microsoft Visual Basic-Entwickler rufen [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) auf, um einen Verweis auf ein [**SecurityCallContext**](securitycallcontext.md) -Objekt zu erhalten, und rufen dann [**issecurityaktivierte**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled)auf, wie im folgenden Beispiel gezeigt:


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



Microsoft Visual C++ Entwickler können [**ISecurityCallContext:: issecurityaktiviert**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) aufrufen, indem Sie [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) aufrufen, um einen Zeiger auf [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) zu erhalten und dann **issecurityaktivierte** aufzurufen. Es folgt ein kurzes Beispiel:


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



Obwohl die bevorzugte Methode zum aufzurufen von [**issecurityaktiviist**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) , das Kontext Objekt für den Sicherheits Rückruf verwendet wird, können Sie **issecurityaktivierte** auch über den Objekt Kontext aufzurufen. (Weitere Informationen finden Sie unter [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) oder [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen von Kontextinformationen für den Sicherheitskontext](accessing-security-call-context-information.md)
</dt> <dt>

[Überprüfen der Rollen Mitgliedschaft](checking-role-membership.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> </dl>

 

 
