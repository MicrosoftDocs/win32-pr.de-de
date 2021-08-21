---
title: Erforderliche Firewall-Ausnahmen für Teredo
description: Damit eine Anwendung Teredo-Datenverkehr empfangen kann, muss die Anwendung IPv6-Datenverkehr in der Hostfirewall empfangen dürfen, und die Anwendung muss die Socketoption IPV6 \_ PROTECTION \_ LEVEL auf "PROTECTION LEVEL \_ \_ UNRESTRICTED" festlegen.
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67d7de38ed91de7d8d8afeada6fe9705ff55f2af1b726ed5c5d49b271464dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354443"
---
# <a name="required-firewall-exceptions-for-teredo"></a>Erforderliche Firewall-Ausnahmen für Teredo

Damit eine Anwendung Teredo-Datenverkehr empfangen kann, muss die Anwendung IPv6-Datenverkehr in der Hostfirewall empfangen dürfen, und die Anwendung muss die Socketoption [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) auf "PROTECTION \_ LEVEL \_ UNRESTRICTED" festlegen. Um diese Art von Szenario zu aktivieren, müssen die in diesem Dokument beschriebenen Firewall-Ausnahmen implementiert werden.

Die folgenden Firewallkonfigurationen sind erforderlich, um eine reibungslose Interoperabilität zwischen einer Firewall und Teredo sicherzustellen:

-   Die Clientfirewall muss die Auflösung von teredo.ipv6.microsoft.com zulassen.
-   UDP-Port 3544 muss geöffnet sein, um sicherzustellen, dass Teredo-Clients erfolgreich mit dem Teredo-Server kommunizieren können.
-   Die Firewall muss dynamische UDP-Ports abrufen, die vom Teredo-Dienst auf dem lokalen Computer verwendet werden, indem die [**FwpmSystemPortsGet0-Funktion**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) aufgerufen wird. Relevante Ports sind vom Typ FWPM \_ SYSTEM \_ PORT \_ TEREDO. Die **FwpmSystemPortsGet0-Funktion** sollte anstelle der jetzt veralteten [**Funktionen GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) oder [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) implementiert werden.
-   Die Firewall ermöglicht dem System das Senden und Empfangen von UDP-/IPv4-Paketen an UDP-Port 1900 im lokalen Subnetz, da dadurch UPnP-Ermittlungsdatenverkehr fließen kann und die Konnektivitätsraten verbessert werden können.
    > [!Note]  
    > Wenn diese Bedingung nicht erfüllt ist, wird das Potenzial für Szenarien eingeführt, in denen Kompatibilitätsprobleme im Zusammenhang mit der Kommunikation zwischen bestimmten NAT-Typen auftreten können. insbesondere zwischen symmetrischen NATs und eingeschränkten NATs. Während symmetrische NATs in Hotspots beliebt sind und eingeschränkte NATs in Heimen beliebt sind, kann die Kommunikation zwischen den beiden aufseiten der eingeschränkten NAT zu Fehlern kommen.

     

-   Eingehende und ausgehende ICMPv6-Ausnahmen "Echo Request" und "Echo Reply" müssen aktiviert sein. Diese Ausnahmen sind erforderlich, um sicherzustellen, dass ein Teredo-Client als hostspezifisches Teredo-Relay fungieren kann. Ein Teredo-hostspezifisches Relay kann durch die zusätzliche native IPv6-Adresse oder eine 6to4-Adresse identifiziert werden, die mit der Teredo-Adresse bereitgestellt wird.

Clientfirewalls müssen die folgenden ICMPv6-Fehlermeldungen und Ermittlungsfunktionen gemäß RFC 4443 unterstützen:



| Code    | BESCHREIBUNG                                    |
|---------|------------------------------------------------|
| 135/136 | ICMPV6 Neighbor-Anforderung und -Ankündigung |
| 133/134 | Routerankündigung und -ankündigung          |
| 128/129 | ICMPV6-Echoanforderung und -antwort                  |
| 1       | Ziel nicht erreichbar                        |
| 2       | Paket zu groß                               |
| 3       | Überschrittene Zeit                                  |
| 4       | Ungültiger Parameter                              |



 

Wenn diese Nachrichten nicht ausdrücklich zugelassen werden können, sollte die Ausnahme aller ICMPv6-Nachrichten in der Firewall aktiviert werden. Darüber hinaus kann die Hostfirewall feststellen, dass die pakete, die mit den Codes 135/136 oder 133/134 klassifiziert sind, vom Benutzermodusdienst **iphlpsvc** und nicht vom Stapel stammen oder darauf ausgerichtet sind. Diese Pakete dürfen nicht von der Hostfirewall gelöscht werden. Der Teredo-Dienst wird hauptsächlich innerhalb des IP-Hilfsdiensts "Benutzermodus" implementiert.

Mithilfe des [**INetFwPolicy2-Windows**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Firewall-API, um alle Regeln aufzuzählen, für die das Edgedurchlaufflag festgelegt ist, werden alle Anwendungen, die auf nicht angeforderten Datenverkehr lauschen möchten, auf die Firewallausnahme aufgeführt. Spezifische Informationen zur Verwendung der Edgedurchlaufoption finden Sie unter [Empfangen von nicht angeforderten Datenverkehr über Teredo](receiving-unsolicited-traffic-over-teredo.md).

Rückrufe sind dem folgenden Beispielenumerationscode nicht zugeordnet. Es wird dringend empfohlen, dass Drittanbieterfirewalls die Enumeration in regelmäßigen Abständen oder immer dann ausführen, wenn die Firewall eine neue Anwendung erkennt, die versucht, die Firewall zu durchlaufen.


```C++
#include <windows.h>
#include <objbase.h>
#include <stdio.h>
#include <atlcomcli.h>
#include <strsafe.h>
#include <netfw.h>

#define NET_FW_IP_PROTOCOL_TCP_NAME L"TCP"
#define NET_FW_IP_PROTOCOL_UDP_NAME L"UDP"

#define NET_FW_RULE_DIR_IN_NAME L"In"
#define NET_FW_RULE_DIR_OUT_NAME L"Out"

#define NET_FW_RULE_ACTION_BLOCK_NAME L"Block"
#define NET_FW_RULE_ACTION_ALLOW_NAME L"Allow"

#define NET_FW_RULE_ENABLE_IN_NAME L"TRUE"
#define NET_FW_RULE_DISABLE_IN_NAME L"FALSE"

#import "netfw.tlb"

void DumpFWRulesInCollection(long Allprofiletypes, NetFwPublicTypeLib::INetFwRulePtr FwRule)
{
    variant_t InterfaceArray;
    variant_t InterfaceString;    

    if(FwRule->Profiles == Allprofiletypes)
    {
        wprintf(L"---------------------------------------------\n");
        wprintf(L"Name:             %s\n", (BSTR)FwRule->Name);        
        wprintf(L"Description:      %s\n", (BSTR)FwRule->Description);
        wprintf(L"Application Name: %s\n", (BSTR)FwRule->ApplicationName);
        wprintf(L"Service Name:     %s\n", (BSTR)FwRule->serviceName);

        switch(FwRule->Protocol)
        {
        case NET_FW_IP_PROTOCOL_TCP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_TCP_NAME);
            break;
        case NET_FW_IP_PROTOCOL_UDP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_UDP_NAME);
            break;
        default:
            break;
        }

        if(FwRule->Protocol != NET_FW_IP_VERSION_V4 && FwRule->Protocol != NET_FW_IP_VERSION_V6)
        {
            wprintf(L"Local Ports:      %s\n", (BSTR)FwRule->LocalPorts);
            wprintf(L"Remote Ports:     %s\n", (BSTR)FwRule->RemotePorts);
        }
        
        wprintf(L"LocalAddresses:   %s\n", (BSTR)FwRule->LocalAddresses);
        wprintf(L"RemoteAddresses:  %s\n", (BSTR)FwRule->RemoteAddresses);
        wprintf(L"Profile:          %d\n", Allprofiletypes);
        

        if(FwRule->Protocol == NET_FW_IP_VERSION_V4 || FwRule->Protocol == NET_FW_IP_VERSION_V6)
        {
            wprintf(L"ICMP TypeCode:    %s\n", (BSTR)FwRule->IcmpTypesAndCodes);
        }

        switch(FwRule->Direction)
        {
        case NET_FW_RULE_DIR_IN:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_IN_NAME);
            break;
        case NET_FW_RULE_DIR_OUT:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_OUT_NAME);
            break;
        default:
            break;
        }

        switch(FwRule->Action)
        {
        case NET_FW_ACTION_BLOCK:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_BLOCK_NAME);
            break;
        case NET_FW_ACTION_ALLOW:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_ALLOW_NAME);
            break;
        default:
            break;
        }
        
        InterfaceArray = FwRule->Interfaces;

        if(InterfaceArray.vt != VT_EMPTY)
        {
            SAFEARRAY    *pSa = NULL;
            long index = 0;

            pSa = InterfaceArray.parray;

            for(long index= pSa->rgsabound->lLbound; index < (long)pSa->rgsabound->cElements; index++)
            {
                SafeArrayGetElement(pSa, &index, &InterfaceString);
                wprintf(L"Interfaces:       %s\n", (BSTR)InterfaceString.bstrVal);
            }
        }
        wprintf(L"Interface Types:  %s\n", (BSTR)FwRule->InterfaceTypes);
        if(FwRule->Enabled)
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_ENABLE_IN_NAME);
        }
        else
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_DISABLE_IN_NAME);
        }
        wprintf(L"Grouping:         %s\n", (BSTR)FwRule->Grouping);
        wprintf(L"Edge:             %s\n", (BSTR)FwRule->EdgeTraversal);
    }
}

int __cdecl main()
{
    HRESULT hr;
    BOOL fComInitialized = FALSE;
    ULONG cFetched = 0; 
    CComVariant var;
    long Allprofiletypes = 0;

    try
    {
        IUnknownPtr pEnumerator = NULL;
        IEnumVARIANT* pVariant = NULL;
        NetFwPublicTypeLib::INetFwPolicy2Ptr sipFwPolicy2;

        //
        // Initialize the COM library on the current thread.
        //
        hr = CoInitialize(NULL);
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        fComInitialized = TRUE;
        
        hr = sipFwPolicy2.CreateInstance("HNetCfg.FwPolicy2");
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        Allprofiletypes = NET_FW_PROFILE2_ALL; // 0x7FFFFFFF
        
        printf("The number of rules in the Windows Firewall are %d\n", sipFwPolicy2->Rules->Count);

        pEnumerator = sipFwPolicy2->Rules->Get_NewEnum();

        if(pEnumerator)
        {
            hr = pEnumerator->QueryInterface(__uuidof(IEnumVARIANT), (void **) &pVariant);
        }

        while(SUCCEEDED(hr) && hr != S_FALSE)
        {        
            NetFwPublicTypeLib::INetFwRulePtr sipFwRule;

            var.Clear();
            hr = pVariant->Next(1, &var, &cFetched);
            if (S_FALSE != hr)
            {
                if (SUCCEEDED(hr))
                {
                    hr = var.ChangeType(VT_DISPATCH);
                }
                if (SUCCEEDED(hr))
                {
                    hr = (V_DISPATCH(&var))->QueryInterface(__uuidof(INetFwRule), reinterpret_cast<void**>(&sipFwRule));
                }

                if (SUCCEEDED(hr))
                {
                    DumpFWRulesInCollection(Allprofiletypes, sipFwRule);
                }
            }
        }
    }
    catch(_com_error& e)
    {
        printf ("Error. HRESULT message is: %s (0x%08lx)\n", e.ErrorMessage(), e.Error());
        if (e.ErrorInfo())
        {
            printf ("Description: %s\n", (char *)e.Description());
        }
    }
    if (fComInitialized)
    {
        CoUninitialize();
    }
    return 0;
}

```



 

 