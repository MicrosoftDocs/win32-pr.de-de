---
title: Grundlegendes zu Routerverwaltungsfunktionen
description: In den folgenden Abschnitten werden die verschiedenen Typen von Routerverwaltungsfunktionen und ihre effektive Verwendung erläutert.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85aac5cc2ec0167527f07c04459ec0aed7dbc248bed727fb4a949765c2fdcc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025400"
---
# <a name="understanding-router-management-functions"></a>Grundlegendes zu Routerverwaltungsfunktionen

In den folgenden Abschnitten werden die verschiedenen Typen von Routerverwaltungsfunktionen und ihre effektive Verwendung erläutert.

Alle Routerverwaltungsfunktionen erfordern Administratorrechte. Ein Benutzer in der Power User-Gruppe verfügt nicht über ausreichende Berechtigungen für die Verwendung der Routerverwaltungsfunktionen.

## <a name="the-different-classes-of-router-management-functions"></a>Die verschiedenen Klassen von Routerverwaltungsfunktionen

Die Routerverwaltungsfunktionen können in die Verwaltungsfunktionen und die Konfigurationsfunktionen unterteilt werden. Die [Verwaltungsfunktionen](router-administration-functions.md) haben das Präfix MprAdmin und die [Konfigurationsfunktionen](router-configuration-functions.md) das Präfix MprConfig. Trotz der Benennung werden beide Sätze von Funktionen für die Routerverwaltung verwendet. Die MprAdmin-Funktionen arbeiten direkt auf dem ausgeführten Router. Die MprConfig-Funktionen verfügen über ähnliche Funktionen, arbeiten jedoch mit der Routerkonfiguration, die in der Registrierung gespeichert ist. Beide Funktionstypen übergeben [Informationsblöcke.](router-information-functions.md)

Die Routerverwaltungsfunktionen können auch basierend darauf aufgeteilt werden, welche Komponenten des Routers sie verwalten: Schnittstellen, Router-Manager oder Router-Manager-Clients.

Die [Routerschnittstellenfunktionen](router-interface-functions.md) haben das Präfix MprAdminInterface oder MprConfigInterface. Verwenden Sie diese Funktionen, um auf Schnittstellen zuzugreifen. Die [Router-Manager-Funktionen](router-manager-transport-functions.md) haben das Präfix MprAdminTransport oder MprConfigTransport. Verwenden Sie diese Funktionen, um auf die Router-Manager zuzugreifen. Schließlich haben die Clientfunktionen des [Router-Managers](router-manager-client-interfacetransport-functions.md) das Präfix MprAdminInterfaceTransport oder MprConfigInterfaceTransport. Verwenden Sie diese Funktionen, um auf die Clients zuzugreifen, die auf dem Router ausgeführt werden.

Eine Teilmenge der MprAdmin-Funktionen sind die [MprAdminMib-Funktionen.](/windows/desktop/RRAS/about-router-management-with-mib) Diese werden auch allein auf der ausgeführten Route ausgeführt. Diese Funktionen übergeben jedoch keine Informationsblöcke. Diese Funktionen bieten dem Protokoll-Designer zusätzliche Flexibilität, insbesondere beim Abrufen von Nichtkonfigurationsinformationen wie Statistiken.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Sicherstellen, dass Änderungen sofort auftreten und persistent sind

Ein Entwickler kann änderungen an der Routerkonfiguration direkt mithilfe der [Routerkonfigurationsfunktionen](router-configuration-functions.md)vornehmen. Änderungen an der Konfiguration werden jedoch erst wirksam, wenn der Router neu gestartet wird, da dies die einzige Zeit ist, in der DIM die Konfiguration aus der Registrierung liest.

Ein Entwickler kann Mithilfe der [Routerverwaltungsfunktionen](router-administration-functions.md)Änderungen am ausgeführten Router vornehmen. Diese Änderungen sind jedoch nicht persistent: Da sie nicht in die Registrierung geschrieben wurden, gehen sie verloren, wenn der Router neu gestartet wird.

Um Änderungen vorzunehmen, die sowohl unmittelbar als auch dauerhaft sind, muss ein Entwickler sowohl die Routerverwaltung als auch die Routerkonfigurationsfunktionen verwenden. Wenn der Router nicht ausgeführt wird, muss der Entwickler nur die entsprechenden Routerkonfigurationsfunktionen aufrufen.

Verwenden Sie zum Abfragen von Informationen vom ausgeführten Router die Routerverwaltungsfunktionen. Wenn der Router nicht ausgeführt wird, fragen Sie Informationen mithilfe der Routerkonfigurationsfunktionen ab.

Die Funktionen [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) und [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) unterstützen die [**MPR \_ INTERFACE \_ 2-Struktur.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) und [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) hingegen nicht. Um eine Nachwahlschnittstelle zu erstellen, die nach einem Neustart persistent ist, rufen Sie **MprAdminInterfaceCreate** mit **MPR \_ INTERFACE \_ 2** auf, und rufen Sie dann **MprConfigInterfaceCreate** mit [**MPR \_ INTERFACE \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) oder [**MPR INTERFACE \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)auf. Um persistente Änderungen an einer Schnittstelle für die Wählanforderungen vorzunehmen, rufen Sie **MprAdminInterfaceSetInfo** mit **MPR \_ INTERFACE \_ 2** auf, und rufen Sie dann **MprConfigInterfaceSetInfo** mit **MPR \_ INTERFACE \_ 0** oder **MPR INTERFACE \_ \_ 1** auf.

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Remote-Verwendung von Routerverwaltungs- und -konfigurationsfunktionen

Die meisten Routerverwaltungs- und Konfigurationsfunktionen können auf einem anderen Computer als dem verwalteten aufgerufen werden. Diese Funktionen verwenden als Parameter, ein Handle für den router-Dienst oder die zu verwaltende Konfiguration. Die Verwaltungsfunktionen verwenden RPC (Remote Procedure Call), um mit dem vom Handle angegebenen Routingdienst zu kommunizieren. Die Konfigurationsfunktionen schreiben in die Registrierung des durch das Handle angegebenen Computers und lesen sie aus der Registrierung.

Um den Routingdienst auf einem Remotecomputer zu verwalten, rufen Sie zunächst [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) auf, um zu überprüfen, ob der Dienst ausgeführt wird. Rufen Sie dann [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) auf, um das Handle abzurufen. Wenn der Routerdienst nicht auf dem Remotecomputer ausgeführt wird, schlagen alle Aufrufe der Routerverwaltung (MprAdmin) fehl.

Um Änderungen an der Routerkonfiguration auf einem Remotecomputer vorzunehmen, rufen Sie ein Handle ab, indem Sie die [**MprConfigServerConnect-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect) aufrufen.

 

 