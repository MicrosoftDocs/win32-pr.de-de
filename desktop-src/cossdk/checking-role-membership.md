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
# <a name="checking-role-membership"></a>Überprüfen der Rollen Mitgliedschaft

Sie können die [**ISecurityCallContext:: isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) -Methode aufrufen, um zu bestimmen, ob der direkte Aufrufer eines Objekts ein Member einer bestimmten Rolle ist. Diese Funktion ist nützlich, wenn Sie sicherstellen möchten, dass ein bestimmter Codeblock nicht ausgeführt wird, wenn der Aufrufer nicht Mitglied einer bestimmten Rolle ist.

Beispielsweise können Sie mit [**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) sicherstellen, dass Transaktionen über einen angegebenen Betrag, z. b. $1000, nur von Mitgliedern einer Manager-Rolle ausgeführt werden. Wenn der Aufrufer kein Manager und die Transaktion über $1000 ist, wird die Transaktion nicht ausgeführt, und es wird eine Fehlermeldung angezeigt.

Die bevorzugte Methode für den Zugriff auf [**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) erfolgt über das Kontext Objekt für den Sicherheits Aufruf, da Sie denselben Verweis auf das Kontext Objekt für den Sicherheits Aufruf zum Abrufen von Sicherheitseigenschaften verwenden können. Sie können jedoch auch über das **ObjectContext** -Objekt auf die **isCallerInRole**-Methode zugreifen. (Weitere Informationen finden Sie unter [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) oder [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)

Wenn Sie Komponenten für eine Microsoft Visual Basic-Anwendung entwickeln, rufen Sie die [**getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) -Funktion auf, und verwenden Sie dann den Sicherheits Aufruf Kontext, um [**isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)aufzurufen, wie im folgenden Beispiel gezeigt:


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



Wenn Sie eine C-oder C++-Anwendung entwickeln, rufen Sie mit [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) einen Zeiger auf die [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) -Schnittstelle ab. Dann rufen Sie [**ISecurityCallContext:: isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)auf, wie im folgenden Beispiel gezeigt:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen von Kontextinformationen für den Sicherheitskontext](accessing-security-call-context-information.md)
</dt> <dt>

[Bestimmen, ob Role-Based Sicherheit aktiviert ist](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> </dl>

 

 
