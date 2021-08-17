---
title: Informationen zur Routerverwaltung mit MIB
description: Die MIB-APIs (Management Information Base) für die Routerverwaltung ermöglichen das Abfragen und Festlegen der Werte von MIB-Variablen, die von einem der Router-Manager oder eines der Routingprotokolle exportiert werden, die vom Router-Manager-Dienst ausgeführt werden.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Routing, Verwaltungsinformationsbasis
- Routing, Verwaltungsinformationsbasis, beschrieben
- Verwaltungsinformationsbasis RRAS
- MIB
- MIB, siehe Verwaltungsinformationsbasis
- Verwaltungsinformationsbasis RRAS
- Management Information Base RRAS , beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a867d903e0fb79f9360dc5f1cb485040ed4489b328365bc2daa063a35fbe27d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792195"
---
# <a name="about-router-management-with-mib"></a>Informationen zur Routerverwaltung mit MIB

Die MIB-APIs (Management Information Base) für die Routerverwaltung ermöglichen das Abfragen und Festlegen der Werte von MIB-Variablen, die von einem der Router-Manager oder eines der Routingprotokolle exportiert werden, die vom Router-Manager-Dienst ausgeführt werden. Mit dieser API unterstützt der Router das Simple Network Management Protocol (SNMP).

Im SNMP-Framework wird jedes der verwaltbaren Objekte im Router durch eine Variable dargestellt, die über einen eindeutigen Objektbezeichner (OID) verfügt. Entsprechend jeder OID ist ein -Wert, der den aktuellen Zustand des -Objekts darstellt. Die Sammlung von OIDs und Werten wird als Verwaltungsinformationsbasis (Management Information Base, MIB) bezeichnet. Die MprAdminMib-Aufrufe ermöglichen es einem Entwickler, ein Objekt über seine OID anzugeben und entweder den Wert des Objekts zu abfragen oder zu schreiben ("Festlegen").

Zum Abfragen und Festlegen von MIB-Variablen muss das Modul, das die Aufrufe unterstützt, einen Satz von Datenstrukturen definieren. Diese Datenstrukturen umfassen Strukturen, die als Objektbezeichner verwendet werden, und Strukturen, die die Werte der MIB-Variablen enthalten, auf die zugegriffen wird. Diese Datenstrukturen sind für alle bis auf den Aufrufer der MIB-Funktion und das Modul, das den Aufruf bedient, nicht transparent.

Das Modul, das den MIB-Aufruf bedient, ist ein Router-Manager oder eines der Routingprotokolle. Der Aufrufer muss auch dann einen Router-Manager angeben, wenn der Aufruf von einem der Routingprotokolle verarbeitet wird. In einem solchen Fall sollte der Aufrufer den Router-Manager angeben, der der Protokollfamilie für dieses Routingprotokoll entspricht. Wenn beispielsweise das OSPF-Routingprotokoll (Open Shortest Path First) den MIB-Aufruf behandeln würde, müsste der Aufrufer den IP-Router-Manager angeben, da OSPF zur IP-Protokollfamilie gehört. In jeder DER MIB-Funktionen gibt der *dwTransportId-Parameter* einen Router-Manager und der *RoutingPid-Parameter* das Routingprotokoll an. Der Router-Manager verfügt auch über ein eindeutiges *RoutingPid,* da einige der MIB-Variablen möglicherweise vom Router-Manager selbst verarbeitet werden.

Die MprAdminMib-Funktionen können auf einem anderen Als dem verwalteten Computer aufgerufen werden. Die MprAdminMIB-Funktionen, die Werte abfragen oder schreiben, verwenden als Parameter ein Handle für den Computer, der verwaltet werden soll. Verwenden Sie [**die MprAdminMIBServerConnect-Funktion,**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) um die Verbindung mit dem Remotecomputer herzustellen und dieses Handle zu erhalten. Rufen Sie nach dem Aufrufen der erforderlichen MprAdminMIB-Funktionen zum Ausführen einer bestimmten administrativen Aufgabe die [**MprAdminMIBServerDisconnect-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) auf, um die Verbindung mit dem Remotecomputer zu beenden.

Die [**Funktionen MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) und [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) nehmen als Parameter eine OID und einen Puffer an, der den neuen Wert für das Objekt enthält.

Die [**Funktionen MprAdminMIBEntryGet,**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget) [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) und [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) nehmen als Parameter eine OID und die Adresse einer Zeigervariablen an. Bei erfolgreicher Rückgabe zeigt die Zeigervariable auf einen Puffer, der den Wert für das -Objekt enthält. Der Aufrufer sollte den Arbeitsspeicher für diesen Puffer durch Aufrufen der [**MprAdminMIBBufferFree-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree) frei geben.

Mit [**den Funktionen MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) und [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) kann ein Entwickler eine *exemplarische SNMP-Datei ausführen.* Da die OIDs geordnet sind, verfügt jede OID und somit jedes verwaltbare Objekt über eine *nächste* OID. Eine SNMP-Exemplarische Vorgehensweise bezieht sich auf das Durchlaufen eines Teils des MIB durch Lesen oder Schreiben einer Sequenz von OIDs.

Alle MprAdminMib-Aufrufe werden über den Dynamic Interface Manager (DIM) übergeben. Je nach OID übergibt DIM den Aufruf an einen der Router-Manager. (SOWOHL IP als auch IPX unterstützen SNMP). Je nach OID kann der Router-Manager den Aufruf selbst verarbeiten oder den Aufruf an einen seiner Clients übergeben. Alle Routerclients müssen die folgenden Funktionen implementieren und exportieren, die den ähnlich benannten MprAdminMIB-Funktionen entsprechen:

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




