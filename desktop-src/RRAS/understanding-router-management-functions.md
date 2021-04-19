---
title: Grundlegendes zu routerverwaltungsfunktionen
description: In den folgenden Abschnitten werden die verschiedenen Typen von routerverwaltungfunktionen erläutert, und Sie sollten wissen, wie Sie diese effektiv verwenden sollten.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b1891bc55b80a18a6d0dd928044da1e0e9709
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341957"
---
# <a name="understanding-router-management-functions"></a>Grundlegendes zu routerverwaltungsfunktionen

In den folgenden Abschnitten werden die verschiedenen Typen von routerverwaltungfunktionen erläutert, und Sie sollten wissen, wie Sie diese effektiv verwenden sollten.

Alle routerverwaltungfunktionen erfordern Administratorrechte. Ein Benutzer in der Hauptbenutzer Gruppe verfügt nicht über ausreichende Berechtigungen für die Verwendung der routerverwaltungfunktionen.

## <a name="the-different-classes-of-router-management-functions"></a>Die verschiedenen Klassen der routerverwaltungfunktionen

Die routerverwaltungfunktionen können in die Verwaltungsfunktionen und die Konfigurationsfunktionen aufgeteilt werden. Die [Verwaltungsfunktionen](router-administration-functions.md) haben das Präfix mpradmin, und die [Konfigurationsfunktionen](router-configuration-functions.md) haben das Präfix mprconfig. Trotz der Benennung werden beide Funktions Sätze für die Routerverwaltung verwendet. Die mpradmin-Funktionen arbeiten direkt auf dem laufenden Router. Die mprconfig-Funktionen verfügen über eine ähnliche Funktionalität, arbeiten jedoch mit der in der Registrierung gespeicherten Routerkonfiguration. Beide Funktionstypen übergeben [Informationsblöcke](router-information-functions.md).

Die routerverwaltungfunktionen können auch basierend auf den Komponenten des Routers, die Sie verwalten, aufgeteilt werden: Schnittstellen, routermanager oder Router-Manager-Clients.

Die [Routerschnittstellen-Funktionen](router-interface-functions.md) haben ein Präfix von mpradmininterface oder mprconfiginterface. Verwenden Sie diese Funktionen für den Zugriff auf Schnittstellen. Die [Router-Manager-Funktionen](router-manager-transport-functions.md) haben das Präfix mpradmintransport oder mprconfigtransport. Verwenden Sie diese Funktionen, um auf die routermanager zuzugreifen. Schließlich haben die [routermanager-Client Funktionen](router-manager-client-interfacetransport-functions.md) ein Präfix von mpradmininterfacetransport oder mprconfiginterfacetransport. Verwenden Sie diese Funktionen, um auf die Clients zuzugreifen, die auf dem Router ausgeführt werden.

Eine Teilmenge der mpradmin-Funktionen sind die [mpradminmib](/windows/desktop/RRAS/about-router-management-with-mib)-Funktionen. Diese werden auch nur auf der laufenden Route betrieben. Diese Funktionen übergeben jedoch keine Informationsblöcke. Diese Funktionen bieten zusätzliche Flexibilität für den Protokoll-Designer, insbesondere zum Abrufen nicht Konfigurationsinformationen, wie z. b. Statistiken.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Sicherstellen, dass Änderungen sofort auftreten und persistent sind

Ein Entwickler kann Änderungen an der Routerkonfiguration direkt mithilfe der [routerkonfigurationsfunktionen](router-configuration-functions.md)vornehmen. Änderungen, die an der Konfiguration vorgenommen wurden, werden jedoch erst wirksam, wenn der Router neu gestartet wird, da dies die einzige Zeit ist, die die Konfiguration aus der Registrierung liest.

Ein Entwickler kann mithilfe der [routerverwaltungsfunktionen](router-administration-functions.md)Änderungen am laufenden Router vornehmen. Diese Änderungen sind jedoch nicht persistent: da Sie nicht in die Registrierung geschrieben wurden, gehen Sie verloren, wenn der Router neu gestartet wird.

Um Änderungen vorzunehmen, die sofort und persistent sind, muss ein Entwickler sowohl die routeradministration als auch die routerkonfigurationsfunktionen verwenden. Wenn der Router nicht ausgeführt wird, muss der Entwickler nur die entsprechenden routerkonfigurationsfunktionen aufzurufen.

Verwenden Sie zum Abfragen von Informationen vom laufenden Router die routerverwaltungsfunktionen. Wenn der Router nicht ausgeführt wird, Fragen Sie Informationen mithilfe der routerkonfigurationsfunktionen ab.

Die [**mpradmininterfacetten ecreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) -und [**mpradmininterfakesetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) -Funktionen unterstützen die [**MPR- \_ Schnittstelle \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) -Struktur. [**Mprconfiginterfacetten ecreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) und [**mprconfiginterfakesetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) hingegen nicht. Um eine Schnittstelle für die Bedarfs gesteuerte Übersetzung zu erstellen, die nach einem Neustart persistent ist, rufen Sie **mpradmininterfakecreate** mit **MPR \_ Interface \_ 2** auf, und rufen Sie dann **mprconfiginterfacetten ecreate** mit [**MPR \_ Interface \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) oder [**MPR \_ Interface \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)auf. Wenn Sie persistente Änderungen an einer Schnittstelle mit Bedarf an Bedarf vornehmen möchten, müssen Sie **mpradmininterfakesetinfo** mit **MPR- \_ Schnittstelle \_ 2** und dann **mprconfiginterfakesetinfo** mit **MPR Interface \_ \_ 0** oder **MPR \_ Interface \_ 1** aufruft.

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Remote Verwendung von routeradministration und Konfigurationsfunktionen

Die meisten routerverwaltungs-und Konfigurationsfunktionen können auf einem anderen Computer als dem verwaltet werden, der nicht verwaltet wird. Diese Funktionen nehmen als Parameter, ein Handle für den zu verwaltenden Routerdienst oder die zu verwaltende Konfiguration. Die Verwaltungsfunktionen verwenden RPC (Remote Prozedur Aufruf) für die Kommunikation mit dem Routing Dienst, der vom handle angegeben wird. Die Konfigurationsfunktionen schreiben in die Registrierung des Computers, der durch das Handle angegeben ist, und lesen diese aus der Registrierung.

Um den Routing Dienst auf einem Remote Computer zu verwalten, wird zuerst [**mpradminisservicerunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) aufgerufen, um zu überprüfen, ob der Dienst ausgeführt wird. Rufen Sie dann [**mpradminserverconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) auf, um das Handle abzurufen. Wenn der Routerdienst nicht auf dem Remote Computer ausgeführt wird, schlagen alle routerverwaltungs-Aufrufe (mpradmin) fehl.

Um Änderungen an der Routerkonfiguration auf einem Remote Computer vorzunehmen, erhalten Sie ein Handle, indem Sie die [**mprconfigserverconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect) -Funktion aufrufen.

 

 