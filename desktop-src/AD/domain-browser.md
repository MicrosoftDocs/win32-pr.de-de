---
title: Domänen Browser
description: Mithilfe der idsbrowsedomaintree-Schnittstelle kann eine Anwendung ein Domänen Browser Dialogfeld anzeigen und den DNS-Namen der vom Benutzer ausgewählten Domäne abrufen.
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- Domänen Browser-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bb932f14544902ab24e8fc1f50daa327bb705
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038763"
---
# <a name="domain-browser"></a>Domänen Browser

Mithilfe der [**idsbrowsedomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Schnittstelle kann eine Anwendung ein Domänen Browser Dialogfeld anzeigen und den DNS-Namen der vom Benutzer ausgewählten Domäne abrufen. Eine Anwendung kann auch die **idsbrowsedomaintree** -Schnittstelle verwenden, um Daten zu allen Domänen Strukturen und Domänen innerhalb einer Gesamtstruktur abzurufen.

Eine Instanz der [**idsbrowsdomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Schnittstelle wird durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit der **CLSID \_ dsdomaintreebrowser** -Klassen Bezeichner erstellt, wie unten gezeigt.

Die [**idsbrowsedomaintree:: setcomputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) -Methode kann verwendet werden, um anzugeben, welcher Computer und welche Anmelde Informationen als Grundlage für das Abrufen der Domänen Daten verwendet werden. Wenn **setcomputer** für eine bestimmte [**idsbrowsedomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Instanz aufgerufen wird, muss [**idsbrowsedomaintree:: flushcacheddomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) aufgerufen werden, bevor **setcomputer** erneut aufgerufen wird.

Die [**idsbrowsdomaintree:: browserto**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) -Methode wird verwendet, um das Dialogfeld Domänen Browser anzuzeigen. Wenn der Benutzer eine Domäne auswählt und auf die Schaltfläche **OK** klickt, gibt **idsbrowst domaintree:: browst** **S \_ OK** zurück, und der *ppsztargetpath* -Parameter enthält den Namen der ausgewählten Domäne. Wenn die namens Zeichenfolge nicht mehr benötigt wird, muss der Aufrufer die Zeichenfolge durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.

Im folgenden Codebeispiel wird gezeigt, wie die [**idsbrowsedomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Schnittstelle verwendet wird, um das Dialogfeld Domänen Browser anzuzeigen.


```C++
#include <shlobj.h>
#include <dsclient.h>

void main(void)
{
    HRESULT     hr;

    hr = CoInitialize(NULL);
    if(FAILED(hr)) 
    {
        return;
    }

    IDsBrowseDomainTree *pDsDomains = NULL;

    hr = ::CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IDsBrowseDomainTree,
                                (void **)(&pDsDomains));
    
    if(SUCCEEDED(hr))
    {
        LPOLESTR    pstr;        

        hr = pDsDomains->BrowseTo(  GetDesktopWindow(),
                                    &pstr,
                                    0);
        
        if(S_OK == hr)
        {
            wprintf(pstr);
            wprintf(L"\n");
            CoTaskMemFree(pstr);
        }

        pDsDomains->Release();
    }

    CoUninitialize();
}
```



Die [**idsbrowcdomaintree:: getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) -Methode wird zum Abrufen von Domänen Strukturdaten verwendet. Die Domänen Daten werden in einer [**domaintree**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) -Struktur bereitgestellt. Die Struktur der **domaintree** enthält die Größe der Struktur und die Anzahl der Domänen Elemente in der Struktur. Die Struktur der **domaintree** enthält auch eine oder mehrere [**domaindesc**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) -Strukturen. **Domaindesc** enthält Daten zu einem einzelnen Element in der Domänen Struktur, einschließlich untergeordneter und gleich geordneter Daten. Die gleich geordneten Elemente einer Domäne können durch Zugriff auf das **pdnextsigend** -Element jeder nachfolgenden **domaindesc** -Struktur aufgelistet werden. Die untergeordneten Elemente der Domäne können auf ähnliche Weise abgerufen werden, indem Sie auf das **pdchildlist** -Member jeder nachfolgenden **domaindesc** -Struktur zugreifen.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie die Domänen Strukturdaten mithilfe der [**idsbrowsedomaintree:: getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) -Methode abrufen und darauf zugreifen können.


```C++
//  Add dsuiext.lib to the project.

#include "stdafx.h"
#include <shlobj.h>
#include <dsclient.h>

//The PrintDomain() function displays the domain name
void PrintDomain(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel)
{
    DWORD i;

    // Display the domain name.
    for(i = 0; i < dwIndentLevel; i++)
    {
        wprintf(L"  ");
    }
    wprintf(pDomainDesc->pszName);
    wprintf(L"\n");
}

//The WalkDomainTree() function traverses the domain tree and prints the current domain name
void WalkDomainTree(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel = 0)
{
    DOMAINDESC  *pCurrent;

    // Walk through the current item and any siblings it may have.
    for(pCurrent = pDomainDesc; 
        NULL != pCurrent; 
        pCurrent = pCurrent->pdNextSibling)
    {
        // Print the current domain name.
        PrintDomain(pCurrent, dwIndentLevel);

        // Walk the child tree, if one exists.
        if(NULL != pCurrent->pdChildList)
        {
            WalkDomainTree(pCurrent->pdChildList, 
                           dwIndentLevel + 1);
        }
    }
}

//  Entry point for application
int main(void)
{
    HRESULT hr;
    IDsBrowseDomainTree *pBrowseTree;
    CoInitialize(NULL);

    hr = CoCreateInstance(CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pBrowseTree);

    if(SUCCEEDED(hr))
    {
        DOMAINTREE  *pDomTreeStruct;
        hr = pBrowseTree->GetDomains(&pDomTreeStruct, 
                                     DBDTF_RETURNFQDN);
        if(SUCCEEDED(hr))
        {
            WalkDomainTree(&pDomTreeStruct->aDomains[0]);
            hr = pBrowseTree->FreeDomains(&pDomTreeStruct);
        }
        pBrowseTree->Release();
    }
    CoUninitialize();
}
```



 

 