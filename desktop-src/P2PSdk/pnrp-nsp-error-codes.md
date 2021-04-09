---
description: PNRP-NSP-Fehler Codes
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: PNRP-NSP-Fehler Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b02959c921c8e3a468cadfa87dba6fb8d3c29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865143"
---
# <a name="pnrp-nsp-error-codes"></a>PNRP-NSP-Fehler Codes

Wenn die Funktion des Namespace Anbieters (NSP) einen **\_ Socketfehler** zurückgibt, muss [WSAGetLastError](winsock-nsp-reference-links.md) zum Abrufen von weiteren Fehlerinformationen verwendet werden. Der PNRP-NSP gibt die folgenden Fehlercodes zurück:



| Begriff                                                                                                                                                                     | BESCHREIBUNG                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ abgebrochen<br/>                                                                         | Ein Vorgang wird abgebrochen.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> WSA \_ E \_ nicht \_ mehr<br/>                                                                         | Die Ergebnisse einer aufgelösten Anforderung sind nicht bereit. Dabei handelt es sich möglicherweise nicht um einen Fehler.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span>ausstehende WSA-e/a \_ \_ <br/>                                                                      | Ein Vorgang ist nicht fertiggestellt.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>WSA \_ nicht \_ genügend Arbeits \_ Speicher<br/>                                                      | Es ist nicht genügend Arbeitsspeicher vorhanden, um eine angegebene Aktion abzuschließen.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>WSA- \_ Vorgang \_ abgebrochen<br/>                                                       | Ein Vorgang wird abgebrochen.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>WSA- \_ PNRP- \_ Cloud \_ deaktiviert<br/>                                                | Ein angegebener cloudName ist deaktiviert.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>Die WSA- \_ PNRP- \_ Cloud wurde \_ nicht \_ gefunden.<br/>                                            | Ein angegebener cloudName ist nicht verfügbar.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>WSA \_ PNRP \_ Cloud \_ ist \_ \_ nur Search<br/>                            | Es wurde versucht, einen Namen in einer Cloud zu registrieren, die so konfiguriert wurde, dass Sie nur aufgelöst wird.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>WSA \_ PNRP- \_ Client ungültige Depot- \_ \_ \_ ID.<br/> | Verwenden von PNRP in einem Depot außerhalb der Standardeinstellung. PNRP funktioniert nur im Standard Depot.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>Ungültige WSA- \_ PNRP- \_ \_ Identität<br/>                                          | Der Zugriff auf eine angegebene Identität ist nicht möglich.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>WSA- \_ PNRP \_ zu \_ stark \_ ausgelastet<br/>                                                  | Ein PeerName kann nicht erstellt werden, da der Computer nicht über die Ressourcen zum Verarbeiten der Anforderung verfügt. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>Wsaefault<br/>                                                                                             | Ein-Vorgang ist im aktuellen Zustand nicht zulässig.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>Wsaabval<br/>                                                                                             | Es wurde ein ungültiger Parameter oder eine Kombination von Parametern angegeben.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>Wsaumetunreach<br/>                                                                              | Eine Verbindung mit dem Netzwerk ist verloren gegangen.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>Wsaenotimplementiert<br/>                                                                  | Eine angegebene Funktionalität wird von PNRP nicht implementiert.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | Eine angegebene Funktionalität wird von PNRP nicht unterstützt.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | Ein Vorgang ist nicht fertiggestellt.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> wsaservice \_ nicht \_ gefunden.<br/>                                                     | Ein angegebener Anbieter, ein Namespace oder eine Dienst-ID werden nicht unterstützt.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>Wsasysnotready<br/>                                                                              | Der Dienst wurde nicht gestartet.<br/>                                                                             |



 

 

 




