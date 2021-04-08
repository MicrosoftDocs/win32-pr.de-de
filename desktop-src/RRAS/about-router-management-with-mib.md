---
title: Informationen zur Routerverwaltung mit MIB
description: Die MIB-APIs (Management Information Base) für die Routerverwaltung ermöglichen es, die Werte von MIB-Variablen abzufragen und festzulegen, die von einem der routermanager oder einem der Routing Protokolle exportiert werden, die der routermanager-Dienst verwendet.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Routing, Verwaltungs Informationsbasis
- Routing, Verwaltungs Informationsbasis, beschrieben
- Verwaltungsinformationen Basis-RRAS
- MIB
- MIB, siehe Verwaltungs Informationsbasis
- Verwaltungsinformationen Basis-RRAS
- Verwaltungsinformationen Basis-RRAS, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e015dacc0b36a00ab62d42c710551aa368aa59e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711207"
---
# <a name="about-router-management-with-mib"></a>Informationen zur Routerverwaltung mit MIB

Die MIB-APIs (Management Information Base) für die Routerverwaltung ermöglichen es, die Werte von MIB-Variablen abzufragen und festzulegen, die von einem der routermanager oder einem der Routing Protokolle exportiert werden, die der routermanager-Dienst verwendet. Wenn Sie diese API verwenden, unterstützt der Router das Simple Network Management-Protokoll (SNMP).

Im SNMP-Framework wird jedes der verwaltbaren Objekte im Router durch eine Variable dargestellt, die über einen eindeutigen Objekt Bezeichner (OID) verfügt. Jede OID entspricht einem Wert, der den aktuellen Zustand des Objekts darstellt. Die Auflistung von OIDs und Werten wird als Management Information Base (MIB) bezeichnet. Der mpradminmib-Aufruf ermöglicht einem Entwickler, ein Objekt anhand seiner OID anzugeben und den Wert des Objekts entweder abzufragen oder zu schreiben ("Set").

Um MIB-Variablen abzufragen und festzulegen, muss das Modul, das die Aufrufe verwendet, eine Reihe von Datenstrukturen definieren. Diese Datenstrukturen enthalten Strukturen, die als Objekt Bezeichner und Strukturen verwendet werden, die die Werte der MIB-Variablen enthalten, auf die zugegriffen wird. Diese Datenstrukturen sind nur für den Aufrufer der MIB-Funktion und das Modul, das den Aufruf verarbeitet, nicht transparent.

Das Modul, das den MIB-Befehl verarbeitet, ist ein routermanager oder eines der Routing Protokolle. Der Aufrufer muss einen routermanager angeben, auch wenn der Aufruf von einem der Routing Protokolle verarbeitet wird. In einem solchen Fall sollte der Aufrufer den routermanager angeben, der der Protokollfamilie für dieses Routing Protokoll entspricht. Wenn z. b. das OSPF (Open kürzeste Path First)-Routing Protokoll den MIB-Aufruf verarbeitet hat, müsste der Aufrufer den IP-routermanager angeben, da OSPF zur IP-Protokollfamilie gehört. In jeder der MIB-Funktionen gibt der Parameter " *dwtransportid* " einen routermanager an, und der *routingpid* -Parameter gibt das Routing Protokoll an. Der routermanager verfügt auch über eine eindeutige *routingpid*, da einige der MIB-Variablen vom Router-Manager selbst behandelt werden können.

Die mpradminmib-Funktionen können auf einem anderen Computer als dem verwalteten Computer aufgerufen werden. Die mpradminmib-Funktionen, die Werte Abfragen oder schreiben, nehmen als Parameter ein Handle für den zu verwaltenden Computer an. Verwenden Sie die [**mpradminmibserverconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) -Funktion, um die Verbindung mit dem Remote Computer herzustellen und dieses Handle abzurufen. Nachdem Sie die erforderlichen mpradminmib-Funktionen zum Ausführen einer bestimmten administrativen Aufgabe aufgerufen haben, rufen Sie die [**mpradminmibserverdisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) -Funktion auf, um die Verbindung mit dem Remote Computer zu beenden.

Die [**mpradminmibentrycreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) -und [**mpradminmibentryset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) -Funktionen akzeptieren als Parameter eine OID und einen Puffer, der den neuen Wert für das Objekt enthält.

Die [**mpradminmibentryget**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget)-, [**mpradminmibentrygetfirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) -und [**mpradminmibentrygetnext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) -Funktionen akzeptieren als Parameter eine OID und die Adresse einer Zeiger Variablen. Bei erfolgreicher Rückgabe zeigt die Zeiger Variable auf einen Puffer, der den Wert für das-Objekt enthält. Der Aufrufer sollte den Speicher für diesen Puffer durch Aufrufen der [**mpradminmibbufferfree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree) -Funktion freigeben.

Die [**mpradminmibentrygetfirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) -Funktion und die [**mpradminmibentrygetnext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) -Funktion ermöglichen einem Entwickler das Ausführen eines *SNMP*-Durchlaufs. Da die OIDs geordnet sind, verfügt jede OID und somit jedes verwaltbare Objekt über eine *nächste* OID. Ein SNMP-Walk bezieht sich auf die Durchquerung eines Teils der MIB durch das Lesen oder Schreiben einer OIDs-Sequenz.

Alle mpradminmib-Aufrufe durchlaufen den Dynamic Interface Manager (Dim). Abhängig von der OID übergibt Dim den-Aufrufer an einen der routermanager. (Sowohl IP als auch IPX unterstützen SNMP). Je nach OID kann der routermanager den eigentlichen Rückruf selbst verarbeiten oder den-Rückruf an einen seiner Clients übergeben. Alle routerclients müssen die folgenden Funktionen implementieren und exportieren, die den ähnlich benannten mpradminmib-Funktionen entsprechen:

-   [**Mibcreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**Mibdelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**Mibset**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**Mibget**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**Mibgetfirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**Mibgetnext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**Mibgettrapinfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**Mibsettrapinfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




