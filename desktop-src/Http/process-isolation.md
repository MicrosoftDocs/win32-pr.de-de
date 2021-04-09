---
title: Prozessisolation
description: Die HTTP Server-API, Version 2,0, bietet die Möglichkeit, einen sichereren und zuverlässigeren Dienst zu erstellen, indem Arbeitsprozesse isoliert werden, die Wartungsanforderungen in der Anforderungs Warteschlange verarbeiten.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efcfccc78bbef435aa0c74e918003383135bc4ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "103869344"
---
# <a name="process-isolation"></a>Prozessisolation

Die HTTP Server-API, Version 2,0, bietet die Möglichkeit, einen sichereren und zuverlässigeren Dienst zu erstellen, indem Arbeitsprozesse isoliert werden, die Wartungsanforderungen in der Anforderungs Warteschlange verarbeiten. Die Anforderungs Warteschlange wird von einem Controller oder Ersteller-Prozess erstellt und verwaltet, der den Zugriff darauf strikt steuert. Der Controller Prozess führt einen oder mehrere separate Arbeitsprozesse aus, die e/a-Vorgänge in der Anforderungs Warteschlange ausführen. Der Controller Prozess wird mit Administratorrechten ausgeführt und konfiguriert die Anforderungs Warteschlange, während der Arbeits Thread mit niedrigerer Berechtigung Zugriffs-und Dienst Anforderungen aus der Anforderungs Warteschlange verarbeitet. Diese Architektur unterstützt die Richtlinie für Anwendungen, die unter "geringsten Berechtigungen" ausgeführt werden, und verringert die Möglichkeit von Sicherheitsrisiken, die durch Code von Drittanbietern entstehen, der möglicherweise in Arbeitsprozessen ausgeführt wird.

Der Zugriff auf die Anforderungs Warteschlange wird gewährt, wenn der Controller Prozess die Anforderungs Warteschlange mit einem Namen und einer Access Control Liste (ACL) erstellt. Webanwendungen, die in der ACL enthalten sind, können eine vorhandene Anforderungs Warteschlange anhand des Namens öffnen. Der Ersteller-Prozess kann auch ein Arbeitsprozess in der Anforderungs Warteschlange sein. Weitere Informationen finden Sie im Thema [benannte Anforderungs Warteschlange](named-request-queue.md) . Das folgende Diagramm zeigt die Architektur einer typischen HTTP-Anwendung, die mit dem Arbeitsprozess Modell ausgeführt wird:

![Diagramm, das die Architektur einer H t t P-Anwendung mithilfe des Arbeitsprozess Modells anzeigt.](images/processisolation.png)

Einzelne Arbeitsprozesse innerhalb der Anwendung sind von anderen Arbeitsprozessen isoliert, und die Integrität der einzelnen Arbeitsprozesse kann vom Controller Prozess überwacht werden. Der Controller Prozess ist von den Workerprozessen isoliert. Die Komponenten der http-Architektur werden im folgenden beschrieben:

-   Ersteller oder Controller Prozess: der Controller Prozess kann mit oder ohne Administratorrechte ausgeführt werden, um die Integrität zu überwachen und den Dienst zu konfigurieren. Der Controller Prozess erstellt in der Regel eine einzelne Server Sitzung für den Dienst und definiert die URL-Gruppen unter der Server Sitzung. Die URL-Gruppe, der eine bestimmte URL zugeordnet ist, bestimmt, welche Anforderungs Warteschlange den Namespace durch die jeweilige URL bezeichnet. Der Controller Prozess erstellt außerdem die Anforderungs Warteschlange und gestartet die Arbeitsprozesse, die auf die Anforderungs Warteschlange zugreifen können.
-   Arbeitsprozess: die vom Controller Prozess gestarteten Arbeitsprozesse führen e/a-Vorgänge in der Anforderungs Warteschlange aus, die den URLs zugeordnet ist, die Sie bedienen. Die Webanwendung erhält Zugriff auf die Anforderungs Warteschlange durch den Controller Prozess in der ACL, wenn die Anforderungs Warteschlange erstellt wird. Wenn die Webanwendung nicht auch der Ersteller-Prozess ist, wird der Dienst nicht verwaltet, oder die Anforderungs Warteschlange wird nicht konfiguriert. Der Controller Prozess kommuniziert den Namen der Anforderungs Warteschlange an den Arbeitsprozess, und der Arbeitsprozess öffnet die Anforderungs Warteschlange anhand des Namens. Arbeitsprozesse können Webanwendungen von Drittanbietern laden, ohne in anderen Teilen der Anwendung Sicherheitsrisiken einzuführen.
-   Anforderungs Warteschlange: die Anforderungs Warteschlange wird vom Controller Prozess erstellt und konfiguriert. Der Controller gibt die Prozesse an, denen der Zugriff auf die Anforderungs Warteschlange in der ACL gestattet ist, wenn die Anforderungs Warteschlange erstellt wird.
-   Server Sitzung: der Controller Prozess erstellt und konfiguriert in der Regel eine einzelne Server Sitzung für die Anwendung. Die Server Sitzung verwaltet die Konfigurations Eigenschaften für die gesamte Anwendung. URL-Gruppen werden durch den Controller Prozess unter der Server Sitzung erstellt.
-   URL-Gruppe: der Controller Prozess erstellt die URL-Gruppen unter der Server Sitzung und konfiguriert die URL-Gruppe unabhängig von der Server Sitzung. Die URLs werden der Gruppe vom Controller Prozess hinzugefügt. Anforderungen werden an die Anforderungs Warteschlange weitergeleitet, der die URL-Gruppe zugeordnet ist.

 

 




