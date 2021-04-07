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
# <a name="domain-browser"></a><span data-ttu-id="397a8-104">Domänen Browser</span><span class="sxs-lookup"><span data-stu-id="397a8-104">Domain Browser</span></span>

<span data-ttu-id="397a8-105">Mithilfe der [**idsbrowsedomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Schnittstelle kann eine Anwendung ein Domänen Browser Dialogfeld anzeigen und den DNS-Namen der vom Benutzer ausgewählten Domäne abrufen.</span><span class="sxs-lookup"><span data-stu-id="397a8-105">Using the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface, an application can display a domain browser dialog box and obtain the DNS name of the domain selected by the user.</span></span> <span data-ttu-id="397a8-106">Eine Anwendung kann auch die **idsbrowsedomaintree** -Schnittstelle verwenden, um Daten zu allen Domänen Strukturen und Domänen innerhalb einer Gesamtstruktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="397a8-106">An application can also use the **IDsBrowseDomainTree** interface to obtain data about all domain trees and domains within a forest.</span></span>

<span data-ttu-id="397a8-107">Eine Instanz der [**idsbrowsdomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Schnittstelle wird durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit der **CLSID \_ dsdomaintreebrowser** -Klassen Bezeichner erstellt, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="397a8-107">An instance of the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface is created by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsDomainTreeBrowser** class identifier as shown below.</span></span>

<span data-ttu-id="397a8-108">Die [**idsbrowsedomaintree:: setcomputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) -Methode kann verwendet werden, um anzugeben, welcher Computer und welche Anmelde Informationen als Grundlage für das Abrufen der Domänen Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="397a8-108">The [**IDsBrowseDomainTree::SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) method can be used to specify which computer and credentials are used as the basis for retrieving the domain data.</span></span> <span data-ttu-id="397a8-109">Wenn **setcomputer** für eine bestimmte [**idsbrowsedomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Instanz aufgerufen wird, muss [**idsbrowsedomaintree:: flushcacheddomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) aufgerufen werden, bevor **setcomputer** erneut aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="397a8-109">When **SetComputer** is called on a particular [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) instance, [**IDsBrowseDomainTree::FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) must be called before **SetComputer** is called again.</span></span>

<span data-ttu-id="397a8-110">Die [**idsbrowsdomaintree:: browserto**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) -Methode wird verwendet, um das Dialogfeld Domänen Browser anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="397a8-110">The [**IDsBrowseDomainTree::BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) method is used to display the domain browser dialog box.</span></span> <span data-ttu-id="397a8-111">Wenn der Benutzer eine Domäne auswählt und auf die Schaltfläche **OK** klickt, gibt **idsbrowst domaintree:: browst** **S \_ OK** zurück, und der *ppsztargetpath* -Parameter enthält den Namen der ausgewählten Domäne.</span><span class="sxs-lookup"><span data-stu-id="397a8-111">When the user selects a domain and clicks the **OK** button, the **IDsBrowseDomainTree::BrowseTo** returns **S\_OK** and the *ppszTargetPath* parameter contains the name of the selected domain.</span></span> <span data-ttu-id="397a8-112">Wenn die namens Zeichenfolge nicht mehr benötigt wird, muss der Aufrufer die Zeichenfolge durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben.</span><span class="sxs-lookup"><span data-stu-id="397a8-112">When the name string is no longer required, the caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

<span data-ttu-id="397a8-113">Im folgenden Codebeispiel wird gezeigt, wie die [**idsbrowsedomaintree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) -Schnittstelle verwendet wird, um das Dialogfeld Domänen Browser anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="397a8-113">The following code example shows how to use the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface to display the domain browser dialog box.</span></span>


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



<span data-ttu-id="397a8-114">Die [**idsbrowcdomaintree:: getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) -Methode wird zum Abrufen von Domänen Strukturdaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="397a8-114">The [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method is used to obtain domain tree data.</span></span> <span data-ttu-id="397a8-115">Die Domänen Daten werden in einer [**domaintree**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) -Struktur bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="397a8-115">The domain data is supplied in a [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) structure.</span></span> <span data-ttu-id="397a8-116">Die Struktur der **domaintree** enthält die Größe der Struktur und die Anzahl der Domänen Elemente in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="397a8-116">The **DOMAINTREE** structure contains the size of the structure and the number of domain elements in the tree.</span></span> <span data-ttu-id="397a8-117">Die Struktur der **domaintree** enthält auch eine oder mehrere [**domaindesc**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="397a8-117">The **DOMAINTREE** structure also contains one or more [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) structures.</span></span> <span data-ttu-id="397a8-118">**Domaindesc** enthält Daten zu einem einzelnen Element in der Domänen Struktur, einschließlich untergeordneter und gleich geordneter Daten.</span><span class="sxs-lookup"><span data-stu-id="397a8-118">The **DOMAINDESC** contains data about a single element in the domain tree, including child and sibling data.</span></span> <span data-ttu-id="397a8-119">Die gleich geordneten Elemente einer Domäne können durch Zugriff auf das **pdnextsigend** -Element jeder nachfolgenden **domaindesc** -Struktur aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="397a8-119">The siblings of a domain can be enumerated by accessing the **pdNextSibling** member of each subsequent **DOMAINDESC** structure.</span></span> <span data-ttu-id="397a8-120">Die untergeordneten Elemente der Domäne können auf ähnliche Weise abgerufen werden, indem Sie auf das **pdchildlist** -Member jeder nachfolgenden **domaindesc** -Struktur zugreifen.</span><span class="sxs-lookup"><span data-stu-id="397a8-120">The children of the domain can be retrieved in a similar manner by accessing the **pdChildList** member of each subsequent **DOMAINDESC** structure.</span></span>

<span data-ttu-id="397a8-121">Im folgenden Codebeispiel wird veranschaulicht, wie Sie die Domänen Strukturdaten mithilfe der [**idsbrowsedomaintree:: getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) -Methode abrufen und darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="397a8-121">The following code example shows how to obtain and access the domain tree data using the [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method.</span></span>


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



 

 