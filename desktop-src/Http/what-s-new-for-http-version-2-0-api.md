---
title: Neuerungen bei der HTTP-Server Version 2,0-API
description: Die folgenden Features sind in der HTTP-Server Version 2,0-API verfügbar.
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- Neuerungen bei der HTTP-Server Version 2,0-API
- HTTP Server-API, Version 2,0, Neuerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 932a27a45768d0cb00cde4cb89fc4e5d424d1f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036579"
---
# <a name="whats-new-for-http-server-version-20-api"></a>Neuerungen bei der HTTP-Server Version 2,0-API

Die HTTP Server-API der Version 2,0 fügt Eigenschaften Konfigurationsobjekte und erweiterte Anforderungs Warteschlangen-Verwaltung hinzu. Weitere Informationen und eine vollständige Liste der Funktionen finden Sie im [Referenz Thema http Server Version 2,0](http-server-api-version-2-0-reference.md) . Die folgenden Features sind in der HTTP-Server Version 2,0-API verfügbar.

## <a name="configuration-objects"></a>Konfigurationsobjekte

Die Konfigurationsobjekte Server Sitzung und URL-Gruppe ermöglichen es Anwendungen, den HTTP-Dienst zu konfigurieren. Die Server Sitzung ist das Konfigurationsobjekt der obersten Ebene, das die Standardeinstellungen der HTTP-Server-API für alle URL-Gruppen überschreibt, die in der Sitzung erstellt wurden. Die URL-Gruppe, die unter einer Server Sitzung erstellt wird, verwaltet einen Satz von URLs, die die Konfigurationseinstellungen für die Gruppe erhalten. Weitere Informationen finden Sie im Thema zur [Architektur der HTTP-Version 2,0](http-version-2-0-architecture.md) .

## <a name="property-configuration-in-version-20"></a>Eigenschaften Konfiguration in Version 2,0

Die Konfiguration wird für die Server Sitzung oder die URL-Gruppen Objekte ausgeführt. Server weite Konfigurationen werden für das Konfigurationsobjekt der Server Sitzung festgelegt. Die URL-Gruppen, die unter der Server Sitzung erstellt werden, erben die Server Sitzungs Konfigurationen. Konfigurationen, die für die URL-Gruppe festgelegt sind, überschreiben die Server Sitzungs Konfigurationen Zu den Konfigurationen, die von der Anwendung festgelegt werden können, zählen Verbindungs Timeouts, Verbindungs Limits, Authentifizierung und Protokollierung. Weitere Informationen finden Sie im Thema [Konfigurieren von Eigenschaften in HTTP-Version 2,0](configuring-properties-in-http-version-2-0.md) .

## <a name="process-isolation-on-request-queues"></a>Prozess Isolation in Anforderungs Warteschlangen

Die Anforderungs Warteschlange der Version 2,0 unterstützt die Prozess Isolation und ermöglicht es mehreren Arbeitsprozessen, e/a in der Anforderungs Warteschlange Die Konfigurations Eigenschaften, die in der Anforderungs Warteschlange festgelegt sind, ermöglichen Anwendungen eine bessere Kontrolle über den Dienst. Mit dem Feature "benannte Anforderungs Warteschlange" können Anwendungen Anforderungs Warteschlangen erstellen und Sie mit Access Control Listen (ACL) sichern. Anwendungen, die mit einem anderen Benutzerkonto als dem Konto ausgeführt werden, das die Anforderungs Warteschlange erstellt hat, können die Anforderungs Warteschlange öffnen, Anforderungen empfangen und Antworten senden. Weitere Informationen finden Sie im Thema [Prozess Isolation](process-isolation.md) .

## <a name="full-kernel-mode-ssl"></a>Vollständiger Kernel Modus-SSL

Die SSL-Sicherheit im Kernel Modus ist standardmäßig aktiviert. Client Zertifikate für die gegenseitige Authentifizierung werden ebenfalls unterstützt. Die Leistung wird verbessert, indem SSL-Vorgänge im Kernel Modus abgeschlossen werden. Dadurch werden die Übergänge zwischen Kernel und Benutzermodus verringert. Weitere Informationen finden Sie im Thema [Kernel Modus SSL](kernel-mode-ssl.md) .

## <a name="kernel-mode-response-cache"></a>Kernel Modus-Antwort Cache

Antworten mit statischem Inhalt können im Kernel Modus zwischengespeichert werden, was eine bessere Leistung im benutzermoduscache bereitstellt. Die Cache Richtlinien Struktur wird mit der Antwort gesendet. Weitere Informationen finden Sie im Thema [Kernel Modus Cache in http 2,0](kernel-mode-cache-in-http-2-0.md) .

## <a name="authentication"></a>Authentifizierung

Die HTTP \_ -Antwort-und HTTP- \_ Anforderungs Strukturen werden aktualisiert, sodass Sie Authentifizierungsinformationen enthalten. Die Server seitige Authentifizierung wird für die folgenden Schemas unterstützt: aushandeln, NTLM, Basic und Digest. Anwendungen können die unterstützten Authentifizierungs Schemas angeben und die bevorzugte Reihenfolge für diese Schemas festlegen.

## <a name="object-scoped-versioning"></a>Objekt Bereichs bezogene Versionsverwaltung

Die API der HTTP-Server Version 1,0 hat die Versionsinformationen im httpinitialize-Rückruf übergeben. Die Version wurde Global für alle Anwendungen im gleichen Prozess festgelegt. In der HTTP-Server Version 2,0-API werden die Versionsinformationen beim Erstellen des Objekts bereitgestellt. Weitere Informationen finden Sie unter [Versionsverwaltung in der HTTP Server-API, Version 2,0](versioning-in-http-2-0.md).

## <a name="logging"></a>Protokollierung

Ab Version 2,0 kann die Protokollierung über die HTTP-Server-API konfiguriert werden. Die für eine Server Sitzung aktivierte Protokollierung dient als zentrale Protokollierung für den Dienst. Die Protokollierung kann auch für eine URL-Gruppe für individualisierte Protokolldateien aktiviert werden. Die Anwendung gibt das Format für die Protokolldateien sowie die Felder an, die für Fehler und erfolgreiche Transaktionen protokolliert werden.

## <a name="graceful-request-queue-shutdown"></a>Ordnungsgemäßes Herunterfahren der Anforderungs

Anwendungen können die Anforderungs Warteschlange Herunterfahren und ausstehende Anforderungen in der Warteschlange ordnungsgemäß verarbeiten, bevor Sie den Anforderungs Warteschlangen Prozess beenden. Wenn die Anforderungs Warteschlange heruntergefahren wird, beendet die HTTP-Server-API die Warteschlange von Anforderungen und leitet ausstehende Anforderungen in der Anforderungs Warteschlange weiter.

## <a name="demand-start-on-a-request-queue"></a>Bedarfs Start in einer Anforderungs Warteschlange

Mit der Funktion zum Starten von Anforderungen in der Anforderungs Warteschlange kann die Controller Anwendung die Arbeitsprozess Instanziierung verzögern, bis die erste Anforderung in der Anforderungs Warteschlange eintrifft. Daher können Anwendungen die Nutzung von Ressourcen so lange vermeiden, bis Sie benötigt werden. Weitere Informationen finden Sie im Thema [Demand Start on Version 2,0 Request Queues](demand-start-on-version-2-0-request-queues.md) .

## <a name="port-sharing"></a>Port Freigabe

HTTP-Server-API-basierte Anwendungen geben den IP-lausch Bereich automatisch für andere nicht-http-Server-API-basierte Anwendungen auf dem Computer frei. die IP-Abhörliste ist nicht mehr erforderlich. Wenn die Anwendung eine URL registriert, lauscht die HTTP-Server-API nur auf die angegebene IP-Adresse und das angegebene Port Paar.

## <a name="etw-support"></a>Etw-Unterstützung

Die erweiterte Ablauf Verfolgung mithilfe der Ereignis Ablauf Verfolgung für Windows (ETW) ermöglicht Anwendungen eine höhere Diagnosefunktion. Die Ereignis Ablauf Verfolgung ist verfügbar für URL-Registrierungen und-Reservierungen, Eigenschaften Konfiguration, Cache Ereignisse, Authentifizierung und Protokollierung, um nur einige zu nennen.

## <a name="performance-counters"></a>Leistungsindikatoren

Mit dem Leistungsindikator Tool können Anwendungen Dienst Zähler abrufen und die Leistung des Dienstanbieter diagnostizieren. Globale Leistungsindikatoren verfolgen die Leistung für den Dienst, Site Zähler verfolgen die Leistung von URL-Gruppen und Anforderungs Warteschlangen-Leistungsindikatoren die Leistung der Anforderungs Warteschlange.

## <a name="international-domain-names-idn"></a>Internationale Domänen Namen (IDN)

Internationalisierte Hosts und Pfad Teile der URL ermöglichen die Registrierung von nicht-ASCII-Domänen Namen und-Pfaden. Die HTTP-Server-API verarbeitet Unicode-URLs, um IDN-Standards einzuhalten.

## <a name="netsh-extensions"></a>Netsh-Erweiterungen

Das Netsh-Hilfsprogramm ersetzt das HttpCfg.exe Tool, das in Windows Server 2003 und Windows XP mit Service Pack 2 (SP2) verfügbar ist. Die Netsh-Erweiterung bietet die Möglichkeit, den HTTP-Dienst zu verwalten, zu diagnostizieren und zu konfigurieren. Administratoren können Server weite Einstellungen Abfragen und konfigurieren, wie z. b. Namespace Registrierungen und SSL-Zertifikate.

 

 




