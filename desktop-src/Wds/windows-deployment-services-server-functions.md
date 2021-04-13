---
title: Server Funktionen der Windows-Bereitstellungs Dienste
description: Die folgenden Funktionen werden mit der PXE-Server-API der Windows-Bereitstellungs Dienste verwendet.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3852ecfd3e51d6375ca8d566f78d019e733808ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388654"
---
# <a name="windows-deployment-services-server-functions"></a>Server Funktionen der Windows-Bereitstellungs Dienste

Die folgenden Funktionen werden mit der PXE-Server-API der Windows-Bereitstellungs Dienste verwendet.



| Funktion                                                           | BESCHREIBUNG                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**Pxeasyncrecvdone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Gibt asynchrone Ergebnisse der Client Anforderung zurück.                                                                                |
| [**Pxedhcpappdoption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Fügt eine DHCP-Option an das Antwortpaket an.                                                                                     |
| [**Pxedhcpappdoptionraw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Fügt eine DHCP-Option an das Antwortpaket an.                                                                                     |
| [**Pxedhcpgetoptionvalue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Ruft einen Optionswert aus einem DHCP-Paket ab.                                                                                  |
| [**Pxedhcpgetvendoroptionvalue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Ruft einen Optionswert aus dem herstellerspezifischen Informationsfeld (43) eines DHCP-Pakets ab.                                    |
| [**Pxedhcpinitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Initialisiert ein Antwortpaket als DHCP-Antwortpaket.                                                                          |
| [**Pxedhcpisvalid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Überprüft, ob ein Paket ein DHCP-Paket ist.                                                                                      |
| [**Pxegetserverinfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Gibt Informationen über den PXE-Server zurück.                                                                                      |
| [**Pxepacketallocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Weist ein Paket zu, das mit der [**pxesendreply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) -Funktion gesendet wird.                                          |
| [**Pxepacketfree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Gibt ein von der [**pxepacketallocate-Funktion zugewiesenes**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate) Paket frei.                                       |
| [**Pxeproviderenumclose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Schließt die Enumeration von Anbietern, die von der [**pxeproviderenumfirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) -Funktion geöffnet wurden.               |
| [**Pxeproviderenumfirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Startet eine Enumeration registrierter Anbieter.                                                                                 |
| [**Pxeproviderenumnext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Listet registrierte Anbieter auf.                                                                                               |
| [**Pxeproviderfreeingefo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Gibt durch die [**pxeproviderenumnext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) -Funktion zugeordnete Arbeitsspeicher frei.                                     |
| [*Pxeproviderinitialize*](pxeproviderinitialize.md)               | Ein Export aus einer Anbieter-DLL (Dynamic Link Library), mit der der Anbieter initialisiert und für den Empfang von Client Anforderungen vorbereitet wird. |
| [**Pxeproviderqueryindex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Gibt den Index des angegebenen Anbieters in der Liste der registrierten Anbieter zurück.                                               |
| [*Pxeproviderrecvrequest*](pxeproviderrecvrequest.md)             | Wird aufgerufen, wenn eine Anforderung von einem Client empfangen wird.                                                                               |
| [**Pxeproviderregister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Registriert einen Anbieter beim System.                                                                                          |
| [*Pxeproviderservicecontrol*](pxeproviderservicecontrol.md)       | Wird aufgerufen, wenn der WDS-Dienst einen Dienst Steuerungs Code empfängt.                                                             |
| [**Pxeproviderationtattribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Gibt Attribute für den Anbieter an.                                                                                         |
| [*Pxeprovidershutdown*](pxeprovidershutdown.md)                   | Wird aufgerufen, um den Anbieter herunterzufahren.                                                                                               |
| [**Pxeproviderunregister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Entfernt einen Anbieter aus der Liste der registrierten Anbieter.                                                                      |
| [**Pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Registriert Rückruf Funktionen für verschiedene Benachrichtigungs Ereignisse.                                                                |
| [**Pxesendreply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Sendet ein Paket an eine Client Anforderung.                                                                                            |
| [**Pxetrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Fügt dem PXE-Protokoll einen Ablauf Verfolgungs Eintrag hinzu.                                                                                             |



 

Der folgende Abschnitt ist ab Windows 8 und Windows Server 2012 verfügbar.

| Funktion                                                               | BESCHREIBUNG                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Fügt eine DHCPv6-Option an das Antwortpaket an.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Fügt eine DHCPv6-Option an das Antwortpaket an.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Ruft einen Optionswert aus einem DHCPv6-Paket ab.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Ruft Optionswerte aus der Option " \_ Vendor \_ OPTS (17)" eines DHCPv6-Pakets ab.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Initialisiert ein Antwortpaket als DHCPv6-Antwortpaket.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Überprüft, ob ein Paket ein gültiges DHCPv6-Paket ist.                                             |
| [**Pxegetserverinfoex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Gibt Informationen über den PXE-Server zurück.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Ermöglicht es einem Anbieter, relayforw-Nachrichten und ihre geschposteten Nachrichten \_ Nachrichten für Relaynachrichten zu analysieren \_ . |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Generiert eine Relay-repl-Nachricht.                                                               |



 

 

 




