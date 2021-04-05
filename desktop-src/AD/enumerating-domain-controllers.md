---
title: Auflisten von Domänen Controllern
description: In früheren Versionen von Windows konnte eine Anwendung nur einen einzigen Domänen Controller in einer Domäne abrufen, indem DsGetDcName aufgerufen wurde.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory das Auflisten von Domänen Controllern Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707697"
---
# <a name="enumerating-domain-controllers"></a><span data-ttu-id="c8017-104">Auflisten von Domänen Controllern</span><span class="sxs-lookup"><span data-stu-id="c8017-104">Enumerating Domain Controllers</span></span>

<span data-ttu-id="c8017-105">In früheren Versionen von Windows konnte eine Anwendung nur einen einzigen Domänen Controller in einer Domäne abrufen, indem [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c8017-105">In earlier versions of Windows, an application could only obtain a single domain controller in a domain by calling [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span></span> <span data-ttu-id="c8017-106">Es gab keine Möglichkeit, vorherzusagen, welcher Domänen Controller abgerufen wird, oder eine Liste der Domänen Controller zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8017-106">There was no way to predict which domain controller would be retrieved or to obtain a list of the domain controllers.</span></span> <span data-ttu-id="c8017-107">Windows ermöglicht einer Anwendung die Enumeration der Domänen Controller in einer Domäne mithilfe der Funktionen [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)und [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="c8017-107">Windows enables an application to enumerate the domain controllers in a domain by using the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta), and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions.</span></span>

<span data-ttu-id="c8017-108">Um einen Domänen Controller aufzulisten, nennen Sie [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span><span class="sxs-lookup"><span data-stu-id="c8017-108">To enumerate a domain controller, call [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span></span> <span data-ttu-id="c8017-109">Diese Funktion übernimmt Parameter, die die Domäne für die Aufzählung und andere Enumerationsoptionen definieren.</span><span class="sxs-lookup"><span data-stu-id="c8017-109">This function takes parameters that define the domain to enumerate and other enumeration options.</span></span> <span data-ttu-id="c8017-110">**Dsgetdcopen** stellt ein domänenenumerationskontext-Handle bereit, das verwendet wird, um den Enumerationsvorgang zu identifizieren, wenn [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) und [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8017-110">**DsGetDcOpen** provides a domain enumeration context handle that is used to identify the enumeration operation when [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) are called.</span></span>

<span data-ttu-id="c8017-111">Die [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) -Funktion wird mit dem domänenaufzählungs-Kontext Handle aufgerufen, um den nächsten Domänen Controller in der-Enumeration abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c8017-111">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function is called with the domain enumeration context handle to retrieve the next domain controller in the enumeration.</span></span> <span data-ttu-id="c8017-112">Wenn diese Funktion zum ersten Mal aufgerufen wird, wird der erste Domänen Controller in der-Enumeration abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c8017-112">The first time this function is called, the first domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="c8017-113">Wenn diese Funktion zum zweiten Mal aufgerufen wird, wird der zweite Domänen Controller in der-Enumeration abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c8017-113">The second time this function is called, the second domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="c8017-114">Dieser Prozess wird wiederholt, bis **dsgetdcnext** **\_ einen Fehler ohne \_ Weitere \_ Elemente** zurückgibt, der das Ende der Enumeration angibt.</span><span class="sxs-lookup"><span data-stu-id="c8017-114">This process is repeated until **DsGetDcNext** returns **ERROR\_NO\_MORE\_ITEMS**, that indicates the end of the enumeration.</span></span>

<span data-ttu-id="c8017-115">Die [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) -Funktion Listet die Domänen Controller in zwei Gruppen auf.</span><span class="sxs-lookup"><span data-stu-id="c8017-115">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function will enumerate the domain controllers in two groups.</span></span> <span data-ttu-id="c8017-116">Die erste Gruppe enthält die Domänen Controller, die den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird, und die zweite Gruppe enthält die Domänen Controller, die nicht den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8017-116">The first group contains the domain controllers that cover the site of the computer where the function is executed and the second group contains the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="c8017-117">Wenn im *optionflags* -Parameter in [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)das Flag **für die DS- \_ Benachrichtigung nach einem \_ \_ Standort \_ Daten** Satz angegeben ist, gibt die Funktion " **dsgetdcnext** " eine Fehlermeldung zurück, die **\_ \_ erkannt** wird, nachdem alle Site spezifischen Domänen Controller abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="c8017-117">If the **DS\_NOTIFY\_AFTER\_SITE\_RECORDS** flag is specified in the *OptionFlags* parameter in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), the **DsGetDcNext** function will return **ERROR\_FILEMARK\_DETECTED** after all of the site-specific domain controllers have been retrieved.</span></span> <span data-ttu-id="c8017-118">**Dsgetdcnext** beginnt dann mit der Enumeration der zweiten Gruppe, die alle Domänen Controller in der Domäne enthält, einschließlich der standortspezifischen Domänen Controller, die in der ersten Gruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c8017-118">**DsGetDcNext** will then begin enumerating the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.</span></span>

<span data-ttu-id="c8017-119">Die Domänen Controller, die den Standort des Computers verarbeiten, auf dem die Funktion ausgeführt wird, werden zuerst aufgelistet, gefolgt von den Domänen Controllern, die nicht den Standort des Computers abdecken, auf dem die Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8017-119">Domain controllers that handle the site of the computer where the function is executed are enumerated first followed by the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="c8017-120">Ein Domänen Controller dient als Abdeckung für einen Standort, wenn der Domänen Controller so konfiguriert ist, dass er sich an diesem Standort befindet, oder wenn sich der Domänen Controller an einem Standort befindet, der in Bezug auf die konfigurierten standortübergreifenden Verknüpfungs Kosten am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="c8017-120">A domain controller is said to cover a site if the domain controller is configured to reside in that site or if the domain controller resides in a site that is nearest to the site in question in terms of the configured inter-site link cost.</span></span> <span data-ttu-id="c8017-121">Wenn Domänen Controller sowohl in der Gruppe der Domänen Controller als auch in der Gruppe der Domänen Controller vorhanden sind, die den Computerstandort nicht abdecken, werden Domänen Controller innerhalb der Gruppe in der Reihenfolge ihrer konfigurierten Prioritäten und Gewichtungen zurückgegeben, die in DNS angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c8017-121">If there are any domain controllers in both the group of domain controllers that cover and the group of domain controllers that do not cover the computer site, domain controllers are returned within the group in order of their configured priorities and weights that are specified in DNS.</span></span> <span data-ttu-id="c8017-122">Domänen Controller mit niedrigerer numerischer Priorität werden zuerst innerhalb einer Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8017-122">Domain controllers that have lower numeric priority are returned within a group first.</span></span> <span data-ttu-id="c8017-123">Wenn in einer Site bezogenen Gruppe eine Untergruppe von mehreren Domänen Controllern mit der gleichen Priorität vorhanden ist, werden Domänen Controller in einer gewichteten zufälligen Reihenfolge zurückgegeben, in der Domänen Controller mit höherer Gewichtung eine höhere Wahrscheinlichkeit haben, zuerst zurückgegeben zu werden.</span><span class="sxs-lookup"><span data-stu-id="c8017-123">If within a site-related group there is a subgroup of several domain controllers with the same priority, domain controllers are returned in a weighted random order where domain controllers with higher weight have more probability to be returned first.</span></span> <span data-ttu-id="c8017-124">Die Standorte, Prioritäten und Gewichtungen werden vom Domänen Administrator konfiguriert, um eine effektive Leistung und einen effektiven Lastenausgleich zwischen mehreren Domänen Controllern in der Domäne zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="c8017-124">The sites, priorities, and weights are configured by the domain administrator to achieve effective performance and load balancing among multiple domain controllers available in the domain.</span></span> <span data-ttu-id="c8017-125">Aus diesem Grund nutzen Anwendungen, die die [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) -Funktionen verwenden, diese Optimierungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="c8017-125">Because of this, applications that use the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)/[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)/[**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions automatically take advantage of these optimizations.</span></span>

<span data-ttu-id="c8017-126">Wenn die Enumeration abgeschlossen ist oder nicht mehr erforderlich ist, muss die Enumeration durch Aufrufen von [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) mit dem domänenaufzählungs Kontext Handle geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c8017-126">When the enumeration is complete or is no longer required, the enumeration must be closed by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) with the domain enumeration context handle.</span></span>

<span data-ttu-id="c8017-127">Zum Zurücksetzen der Enumeration ist es erforderlich, die aktuelle Enumeration durch Aufrufen von [**dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) zu schließen und die Enumeration dann erneut zu öffnen, indem Sie erneut [**dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8017-127">To reset the enumeration, it is necessary to close the current enumeration by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) and then reopen the enumeration by calling [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) again.</span></span>

## <a name="example"></a><span data-ttu-id="c8017-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c8017-128">Example</span></span>

<span data-ttu-id="c8017-129">Im folgenden Codebeispiel wird gezeigt, wie diese Funktionen verwendet werden, um die Domänen Controller in der lokalen Domäne aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="c8017-129">The following code example shows how to use these functions to enumerate the domain controllers in the local domain.</span></span>


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




