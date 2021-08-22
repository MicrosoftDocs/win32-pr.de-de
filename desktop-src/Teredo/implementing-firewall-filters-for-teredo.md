---
title: Implementieren von Firewallfiltern für Teredo
description: Windows ermöglicht Anwendungen das Festlegen einer Socketoption, mit der Anwendungen eine explizite Absicht angeben können, Teredo-Datenverkehr zu empfangen, der über die Windows Filterplattform an die Hostfirewall gesendet wird.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe854b210e6b07f0777a492d5c952f502e2f7c2b6c1c4b40497bad3a9e8248a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001808"
---
# <a name="implementing-firewall-filters-for-teredo"></a>Implementieren von Firewallfiltern für Teredo

Windows ermöglicht Anwendungen das Festlegen einer Socketoption, mit der Anwendungen eine explizite Absicht angeben können, Teredo-Datenverkehr zu empfangen, der über die Windows Filterplattform an die Hostfirewall gesendet wird. In Windows wird eine Socketoption zum Festlegen einer Schutzebene verwendet, damit eine Anwendung definieren kann, welche Art von Datenverkehr sie empfangen möchte. Genauer gesagt wird in Szenarien mit Teredo-Datenverkehr die Socketoption [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) angegeben. Es wird empfohlen, dass Hostfirewallimplementierungen die folgenden Filter beibehalten, um Teredo-Datenverkehr für eine Anwendung selektiv zuzulassen, während der Datenverkehr standardmäßig für jede Anwendung ohne Ausnahme blockiert wird.

## <a name="default-block-filter-for-edge-traversed-traffic"></a>Standardblockfilter für Edgedurchlaufdatenverkehr

Eine Hostfirewall muss immer einen Standardblockfilter innerhalb der ALE \_ AUTH \_ RECV \_ ACCEPT \_ V6-Filterebene für Datenverkehr beibehalten, der den angegebenen **Schnittstellentyp- Tunnel** und **Tunnel Teredo-Bedingungen** entspricht. Bei implementierung gibt dieser Filter das Vorhandensein einer Durchlauf-fähigen Edgehostfirewall im System an. Dieser Filter wird als API-Vertrag zwischen der Hostfirewall und Windows angezeigt. Standardmäßig blockiert dieser Filter datenverkehrsgetrahte Edgedatenverkehr an eine beliebige Anwendung.

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> Die Klassen "Delivery", "Arrival" und "Next Hop" von Schnittstellenbedingungen werden verwendet, um ein schwaches Hostmodell und die Paketweiterleitung schnittstellenübergreifend zu steuern. Im obigen Beispiel wird die Delivery-Klasse verwendet. Lesen Sie [filtering conditions Available at Each Filtering Layer (Verfügbare Filterbedingungen für jede Filterebene)](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) in der WFP SDK-Dokumentation, da Ihr Sicherheitsentwurf jeden Fall berücksichtigen muss.

 

## <a name="allow-filter-for-exempt-applications"></a>Filter für ausgenommene Anwendungen zulassen

Wenn eine Anwendung vom Empfang von Teredo-Datenverkehr in einem Lauschsocket ausgenommen ist, muss ein Zulassungsfilter innerhalb der Filterebene ALE \_ AUTH \_ RCV \_ ACCEPT \_ V6 in der Hostfirewall implementiert werden. Beachten Sie, dass die Hostfirewall abhängig davon, wie die Ausnahme vom Benutzer oder der Anwendung konfiguriert wird, eine Socketoption enthalten kann.

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a>Ruhezustands-Calloutfilter

Der Teredo-Dienst in Windows implementiert ein Ruhezustandsmodell. Wenn zu einem bestimmten Zeitpunkt keine Anwendungen an einem UDP- oder TCP-Socket lauschen, für den der Edgedurchlauf aktiviert ist, wechselt der Dienst in einen ruhenden Zustand. Damit der Ruhemechanismus funktioniert, muss die Hostfirewall einen Aufruffilter für jede ausgenommene Anwendung beibehalten, die in der Filterebene ALE \_ AUTH \_ LISTEN \_ V6 für TCP und ALE \_ RESOURCE ASSIGNMENT \_ \_ V6 für UDP-basierte Anwendungen angegeben ist. Im folgenden Beispiel wird ein Ruhezustandsaufruf für eine **TCP-Anwendung** veranschaulicht.

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 