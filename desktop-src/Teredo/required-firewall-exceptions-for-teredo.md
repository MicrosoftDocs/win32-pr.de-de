---
title: Erforderliche Firewallausnahmen für Teredo
description: Damit eine Anwendung Teredo-Datenverkehr empfängt, muss die Anwendung in der Host Firewall den IPv6-Datenverkehr empfangen können, und die Anwendung muss die Socketoption IPv6- \_ Schutz \_ Ebene auf "Schutz \_ Ebene \_ uneingeschränkt" festlegen.
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340280"
---
# <a name="required-firewall-exceptions-for-teredo"></a>Erforderliche Firewallausnahmen für Teredo

Damit eine Anwendung Teredo-Datenverkehr empfängt, muss die Anwendung in der Host Firewall den IPv6-Datenverkehr empfangen können, und die Anwendung muss die Socketoption [IPv6- \_ Schutz \_ Ebene](/windows/desktop/WinSock/ipv6-protection-level) auf "Schutz \_ Ebene \_ uneingeschränkt" festlegen. Um diese Art von Szenario zu aktivieren, müssen die in diesem Dokument beschriebenen Firewallausnahmen implementiert werden.

Die folgenden Firewallkonfigurationen sind erforderlich, um eine reibungslose Interoperabilität zwischen einer Firewall und Teredo sicherzustellen:

-   Die Client Firewall muss die Auflösung von Teredo.IPv6.Microsoft.com zulassen.
-   Der UDP-Port 3544 muss geöffnet sein, um sicherzustellen, dass Teredo-Clients erfolgreich mit dem Teredo-Server kommunizieren können.
-   Die Firewall muss dynamische UDP-Ports abrufen, die vom Teredo-Dienst auf dem lokalen Computer verwendet werden, indem die [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) -Funktion aufgerufen wird. relevante Ports sind vom Typ "swpm \_ \_ Systemport \_ Teredo". Die **FwpmSystemPortsGet0** -Funktion sollte anstelle der nun als veraltet markierten Funktionen [**getteredoport**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) oder [**notifyteredoportchange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) implementiert werden.
-   Die Firewall ermöglicht dem System, UDP/IPv4-Pakete an den UDP-Port 1900 im lokalen Subnetz zu senden und zu empfangen, da dadurch der UPnP-Discovery-Datenverkehr weitergeleitet werden kann und die konnektivitätsraten verbessert werden können.
    > [!Note]  
    > Wenn diese Bedingung nicht erfüllt ist, wird das Potenzial von Szenarien mit der Kommunikation zwischen bestimmten NAT-Typen verursacht. speziell zwischen symmetrischen NATs und eingeschränkten NATs. Obwohl symmetrische NATs in Hotspots beliebt sind und eingeschränkte NATs in Heimen beliebt sind, kann die Kommunikation zwischen den beiden möglicherweise auf der Seite der eingeschränkten NAT fehlerhaft sein.

     

-   Eingehende und ausgehende ICMPv6 "Echo Request"-und "Echo Reply"-Ausnahmen müssen aktiviert sein. Diese Ausnahmen sind erforderlich, um sicherzustellen, dass ein Teredo-Client als Host spezifisches Teredo-Relay fungieren kann. Ein Host spezifisches Teredo-Relay kann durch die zusätzliche systemeigene IPv6-Adresse oder eine IPv6-zu-IPv4-Adresse identifiziert werden, die mit der Teredo-Adresse angegeben wird.

Client Firewalls müssen die folgenden ICMPv6-Fehlermeldungen und Ermittlungs Funktionen pro RFC 4443 unterstützen:



| Code    | BESCHREIBUNG                                    |
|---------|------------------------------------------------|
| 135/136 | ICMPV6 Nachbar Anfrage und Ankündigung |
| 133/134 | Routeranfrage und Ankündigung          |
| 128/129 | ICMPV6-Echo Anforderung und-Antwort                  |
| 1       | Ziel nicht erreichbar                        |
| 2       | Paket zu groß                               |
| 3       | Zeitüberschreitung                                  |
| 4       | Ungültiger Parameter                              |



 

Wenn diese Nachrichten nicht ausdrücklich zulässig sind, sollte die Ausnahme aller ICMPv6-Nachrichten für die Firewall aktiviert werden. Außerdem bemerkt die Host Firewall möglicherweise, dass die durch die Codes 135/136 oder 133/134 klassifizierten Pakete vom Benutzermodusdienst **iphlpsvc** und nicht vom Stapel stammen. Diese Pakete dürfen von der Host Firewall nicht gelöscht werden. Der Teredo-Dienst wird primär im IP-Hilfsdienst "Benutzermodus" implementiert.

Mithilfe der [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) -Windows-Firewall-API können Sie alle Regeln mit dem festgelegten Edge-Traversal-Flag auflisten. alle Anwendungen, die auf nicht angeforderten Datenverkehr lauschen möchten, werden für die Firewallausnahme aufgelistet. Ausführliche Informationen zur Verwendung der Option Edgeausnahme finden Sie unter empfangen von nicht [angefordertem Datenverkehr über Teredo](receiving-unsolicited-traffic-over-teredo.md).

Rückrufe sind nicht mit dem folgenden beispielenumerationscode verknüpft. Es wird dringend empfohlen, dass Drittanbieter Firewalls die Enumeration regelmäßig ausführen oder wenn die Firewall eine neue Anwendung erkennt, die versucht, die Firewall zu durchlaufen.


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



 

 