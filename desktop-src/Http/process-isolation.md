---
title: Prozessisolation
description: Die HTTP Server-API Version 2.0 bietet die Möglichkeit, einen sichereren, zuverlässigeren Dienst zu erstellen, indem Workerprozesse, die Anforderungen in der Anforderungswarteschlange bedienen, isolieren.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025e0829e020740aeeaf0381849b68bfde8b8244e845f9b5f24347bfa6bec1d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830075"
---
# <a name="process-isolation"></a>Prozessisolation

Die HTTP Server-API Version 2.0 bietet die Möglichkeit, einen sichereren, zuverlässigeren Dienst zu erstellen, indem Workerprozesse, die Anforderungen in der Anforderungswarteschlange bedienen, isolieren. Die Anforderungswarteschlange wird von einem Controller- oder Erstellerprozess erstellt und verwaltet, der den Zugriff darauf streng steuert. Der Controllerprozess startet einen oder mehrere separate Workerprozesse, die E/A-Vorgänge in der Anforderungswarteschlange ausführen. Der Controllerprozess wird mit Administratorrechten ausgeführt und konfiguriert die Anforderungswarteschlange, während der Worker mit niedrigeren Berechtigungen Zugriffs- und Dienstanforderungen aus der Anforderungswarteschlange verarbeitet. Diese Architektur unterstützt die Richtlinie von Anwendungen, die unter "geringsten Rechten" ausgeführt werden, und verringert die Wahrscheinlichkeit von Sicherheitsrisiken, die durch Drittanbietercode eingeführt werden, der möglicherweise in Workerprozessen ausgeführt wird.

Der Zugriff auf die Anforderungswarteschlange wird gewährt, wenn der Controllerprozess die Anforderungswarteschlange mit einem Namen und Access Control List (ACL) erstellt. Webanwendungen, die in der ACL enthalten sind, können eine vorhandene Anforderungswarteschlange nach Namen öffnen. Der Erstellerprozess kann auch ein Arbeitsprozess in der Anforderungswarteschlange sein. Weitere Informationen finden Sie im Thema [Benannte Anforderungswarteschlange.](named-request-queue.md) Das folgende Diagramm zeigt die Architektur einer typischen HTTP-Anwendung, die mit dem Workerprozessmodell ausgeführt wird:

![Diagramm, das die Architektur einer H T T P-Anwendung mithilfe des Arbeitsprozessmodells zeigt.](images/processisolation.png)

Einzelne Workerprozesse innerhalb der Anwendung sind von anderen Workerprozessen isoliert, und die Integrität der einzelnen Workerprozesse kann vom Controllerprozess überwacht werden. Der Controllerprozess ist von den Workerprozessen isoliert. Die Komponenten der HTTP-Architektur werden unten beschrieben:

-   Ersteller- oder Controllerprozess: Der Controllerprozess kann mit oder ohne Administratorrechte ausgeführt werden, um die Integrität zu überwachen und den Dienst zu konfigurieren. Der Controllerprozess erstellt in der Regel eine einzelne Serversitzung für den Dienst und definiert die URL-Gruppen unter der Serversitzung. Die URL-Gruppe, der eine bestimmte URL zugeordnet ist, bestimmt, welche Anforderungswarteschlange den Namespace unterstützt, der durch die bestimmte URL bezeichnet wird. Der Controllerprozess erstellt auch die Anforderungswarteschlange und startet die Arbeitsprozesse, die auf die Anforderungswarteschlange zugreifen können.
-   Workerprozess: Die vom Controllerprozess gestarteten Workerprozesse führen E/A für die Anforderungswarteschlange aus, die den urLs zugeordnet ist, die sie verarbeiten. Der Webanwendung wird beim Erstellen der Anforderungswarteschlange zugriff auf die Anforderungswarteschlange durch den Controllerprozess in der ACL gewährt. Sofern die Webanwendung nicht auch der Erstellerprozess ist, wird der Dienst nicht verwaltet oder die Anforderungswarteschlange konfiguriert. Der Controllerprozess übermittelt den Namen der Anforderungswarteschlange an den Arbeitsprozess, und der Arbeitsprozess öffnet die Anforderungswarteschlange nach Namen. Workerprozesse können Webanwendungen von Drittanbietern laden, ohne Sicherheitslücken in anderen Teilen der Anwendung auszunutzen.
-   Anforderungswarteschlange: Die Anforderungswarteschlange wird vom Controllerprozess erstellt und konfiguriert. Der Controller gibt die Prozesse an, die beim Erstellen der Anforderungswarteschlange Zugriff auf die Anforderungswarteschlange in der ACL erhalten.
-   Serversitzung: Der Controllerprozess erstellt und konfiguriert in der Regel eine einzelne Serversitzung für die Anwendung. Die Serversitzung verwaltet die Konfigurationseigenschaften für die gesamte Anwendung. URL-Gruppen werden in der Serversitzung vom Controllerprozess erstellt.
-   URL-Gruppe: Der Controllerprozess erstellt die URL-Gruppen unter der Serversitzung und konfiguriert die URL-Gruppe unabhängig von der Serversitzung. URLs werden der Gruppe durch den Controllerprozess hinzugefügt. Anforderungen werden an die Anforderungswarteschlange geroutet, der die URL-Gruppe zugeordnet ist.

 

 




