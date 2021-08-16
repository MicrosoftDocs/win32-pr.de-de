---
title: Windows Serverfunktionen für Bereitstellungsdienste
description: Die folgenden Funktionen werden mit Windows Deployment Services-PXE-Server-API verwendet.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cc99f01dc88fce91beafe51a65f8e8ddccfdf08c4361fb194a7e60451a5aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330603"
---
# <a name="windows-deployment-services-server-functions"></a>Windows Serverfunktionen für Bereitstellungsdienste

Die folgenden Funktionen werden mit Windows Deployment Services-PXE-Server-API verwendet.



| Funktion                                                           | Beschreibung                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Gibt asynchrone Ergebnisse der Clientanforderung zurück.                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Fügt eine DHCP-Option an das Antwortpaket an.                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Fügt eine DHCP-Option an das Antwortpaket an.                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Ruft einen Optionswert aus einem DHCP-Paket ab.                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Ruft einen Optionswert aus dem Feld Anbieterspezifische Informationen (43) eines DHCP-Pakets ab.                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Initialisiert ein Antwortpaket als DHCP-Antwortpaket.                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Überprüft, ob ein Paket ein DHCP-Paket ist.                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Gibt Informationen zum PXE-Server zurück.                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Ordnet ein Paket zu, das mit der [**PxeSendReply-Funktion**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) gesendet werden soll.                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Gibt ein von der [**PxePacketAllocate-Funktion zugeordnetes**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate) Paket frei.                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Schließt die Enumeration der Von der [**PxeProviderEnumFirst-Funktion geöffneten**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) Anbieter.               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Startet eine Enumeration registrierter Anbieter.                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Listet registrierte Anbieter auf.                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Gibt von der [**PxeProviderEnumNext-Funktion**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) belegten Arbeitsspeicher frei.                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | Ein Export aus einer Anbieter-DLL (Dynamic Link Library), die den Anbieter initialisiert und für den Empfang von Clientanforderungen vorbereitet. |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Gibt den Index des angegebenen Anbieters in der Liste der registrierten Anbieter zurück.                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | Wird aufgerufen, wenn eine Anforderung von einem Client empfangen wird.                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Registriert einen Anbieter beim System.                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | Wird aufgerufen, wenn ein Dienststeuerungscode vom WDS-Dienst empfangen wird.                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Gibt Attribute für den Anbieter an.                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | Wird aufgerufen, um den Anbieter herunterzufahren.                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Entfernt einen Anbieter aus der Liste der registrierten Anbieter.                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Registriert Rückruffunktionen für verschiedene Benachrichtigungsereignisse.                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Sendet ein Paket an eine Clientanforderung.                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Fügt dem PXE-Protokoll einen Ablaufverfolgungseintrag hinzu.                                                                                             |



 

Folgendes ist ab Windows 8 und Windows Server 2012 verfügbar.

| Funktion                                                               | Beschreibung                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Fügt eine DHCPv6-Option an das Antwortpaket an.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Fügt eine DHCPv6-Option an das Antwortpaket an.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Ruft einen Optionswert aus einem DHCPv6-Paket ab.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Ruft Optionswerte aus dem Feld OPTION \_ VENDOR \_ OPTS (17) eines DHCPv6-Pakets ab.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Initialisiert ein Antwortpaket als DHCPv6-Antwortpaket.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Überprüft, ob ein Paket ein gültiges DHCPv6-Paket ist.                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Gibt Informationen zum PXE-Server zurück.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Ermöglicht einem Anbieter das Analysieren von RELAY-FORW-Nachrichten und deren geschachtelten OPTION \_ RELAY \_ MSG-Nachrichten. |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Generiert eine RELAY-REPL-Nachricht.                                                               |



 

 

 




