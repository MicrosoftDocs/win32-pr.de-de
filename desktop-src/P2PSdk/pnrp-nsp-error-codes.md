---
description: PNRP-NSP-Fehlercodes
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: PNRP-NSP-Fehlercodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acee7465a86d56af9b2e07a1ae6948dd1b1a1e9145cee2165b7dd4e90f2a5f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061349"
---
# <a name="pnrp-nsp-error-codes"></a>PNRP-NSP-Fehlercodes

Wenn die NSP-Funktion (Namespace Provider) einen **SOCKET \_ ERROR** zurückgibt, muss [WSAGetLastError](winsock-nsp-reference-links.md) verwendet werden, um weitere Fehlerinformationen abzurufen. Der PNRP-NSP gibt die folgenden Fehlercodes zurück:



| Begriff                                                                                                                                                                     | BESCHREIBUNG                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ CANCELLED<br/>                                                                         | Ein Vorgang wird abgebrochen.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> WSA \_ E \_ NICHT \_ MEHR<br/>                                                                         | Die Ergebnisse einer aufgelösten Anforderung sind nicht bereit. Dies ist möglicherweise kein Fehler.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span> WSA \_ IO \_ PENDING <br/>                                                                      | Ein Vorgang ist nicht abgeschlossen.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>WSA \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER<br/>                                                      | Es ist nicht genügend Arbeitsspeicher vorhanden, um eine angegebene Aktion abzuschließen.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>\_WSA-VORGANG \_ ABGEBROCHEN<br/>                                                       | Ein Vorgang wird abgebrochen.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>WSA \_ PNRP \_ CLOUD \_ DISABLED<br/>                                                | Ein angegebener Cloudname ist deaktiviert.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>WSA \_ PNRP \_ CLOUD NICHT \_ \_ GEFUNDEN<br/>                                            | Ein angegebener Cloudname ist nicht verfügbar.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>WSA \_ PNRP \_ CLOUD \_ IS \_ SEARCH \_ ONLY<br/>                            | Es wurde versucht, einen Namen in einer Cloud zu registrieren, die so konfiguriert wurde, dass er nur aufgelöst wird.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>\_ \_ \_ UNGÜLTIGE \_ \_ DEPOT-ID DES WSA PNRP-CLIENTS<br/> | Verwenden von PNRP in einem Depot außerhalb des Standardwerts. PNRP funktioniert nur im Standardde depot.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>UNGÜLTIGE WSA \_ \_ \_ PNRP-IDENTITÄT<br/>                                          | Auf eine angegebene Identität kann nicht zugegriffen werden.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>WSA \_ PNRP \_ ZU VIEL \_ \_ LAST<br/>                                                  | Ein Peername kann nicht erstellt werden, da der Computer nicht über die Ressourcen zum Verarbeiten der Anforderung verfügt. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | Ein Vorgang ist im aktuellen Zustand nicht zulässig.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | Ein ungültiger Parameter oder eine Kombination von Parametern wird angegeben.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | Eine Verbindung mit dem Netzwerk geht verloren.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | Eine angegebene Funktionalität wird von PNRP nicht implementiert.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | Eine angegebene Funktionalität wird von PNRP nicht unterstützt.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWULEDBLOCK<br/>                                                                              | Ein Vorgang ist nicht abgeschlossen.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> WSASERVICE \_ NICHT \_ GEFUNDEN<br/>                                                     | Ein angegebener Anbieter, Namespace oder dienst-ID wird nicht unterstützt.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | Der Dienst wird nicht gestartet.<br/>                                                                             |



 

 

 




