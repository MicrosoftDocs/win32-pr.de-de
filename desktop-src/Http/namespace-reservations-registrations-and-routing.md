---
title: Namespace Reservierungen, Registrierungen und Routing
description: Reservierungen und Registrierungen sind Vorgänge, mit denen die HTTP-Server-API Zugriff auf den URL-Namespace auf einem Computer gewährt.
ms.assetid: dc66960b-36cd-4c09-be0a-3aec9a8a25d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00801629b5b778bb6c87a0bff615cb9d5618f57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311093"
---
# <a name="namespace-reservations-registrations-and-routing"></a>Namespace Reservierungen, Registrierungen und Routing

Reservierungen und Registrierungen sind Vorgänge, mit denen die HTTP-Server-API Zugriff auf den URL-Namespace auf einem Computer gewährt. Anwendungen können sich für einen Teil des URL-Namespace registrieren, um Anforderungen von HTTP-Clients zu bedienen. Die Anwendung registriert einen Namespace mit der HTTP-Server-API unter Verwendung der [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl) -Funktion. Die HTTP-Server-API fügt die URLs der Anforderungs Warteschlange für die Anwendung hinzu und leitet Anforderungen an die Anwendungen weiter, abhängig von den URLs in ihren Warteschlangen. Bevor die Anwendung sich für den Empfang von Anforderungen für einen URL-Namespace registrieren kann, muss der Systemadministrator eine Reservierung für diese URL für den Benutzer vornehmen, der die Anwendung ausführt. Standardmäßig ist der Namespace geschlossen, d. h. nur der Administrator kann URLPrefixes registrieren, bis der Administrator eine Reservierung eingibt.

Eine Reservierung weist den einzelnen Benutzern permanent einen Teil des URL-Namespace zu, sodass Sie diesen Teil des Namespaces reservieren oder "besitzen" können. Durch Reservierungen erhält der Benutzer das Recht, sich bei Service Requests für den Namespace zu registrieren. Die HTTP-Server-API stellt sicher, dass Benutzer keine URLs aus Teilen des Namespace registrieren, die Sie nicht besitzen. Um die Namespace Sicherheit sicherzustellen, werden ACLs (Access Control Liste) auf den Teil des Namespaces angewendet, der für die einzelnen Benutzer reserviert ist.

Reservierte Namespaces werden durch URL-Präfix Zeichenfolgen identifiziert, die auf die gleiche Weise wie URL-Präfixe für Registrierungen formatiert sind. Dies bedeutet, dass alle unterschiedlichen hostspezifiziererkategorien auch für Reservierungen verfügbar sind.

Namespace Reservierungen werden über Neustarts hinweg beibehalten, und Änderungen werden dynamisch wirksam, sodass der Computer nicht beendet und neu gestartet werden muss.

Die folgenden Konzepte werden weiter erläutert, da Sie sich auf den Prozess der Registrierung und Reservierung von Namespaces beziehen.

-   Nummern. Die Registrierung ist der Vorgang, mit dem eine Anwendung Interesse an dem Empfang von Anforderungen für ein bestimmtes URLPrefix-Präfix angibt. Die API für die URL-Registrierung ist [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl). Die Registrierung erfolgt in der Regel während des Starts der Anwendung und muss bei jedem Start der Anwendung ausgeführt werden.
-   Routing. Das Routing wird von der HTTP-Server-API durchgeführt, um zu bestimmen, an welche Anwendung die Anforderung weitergeleitet werden soll, basierend auf dem am besten geeigneten [URLPrefix](urlprefix-strings.md) , das registriert und/oder reserviert ist. Beim Routing Vorgang werden sowohl Registrierungs-als auch Reservierungs Informationen verwendet.
-   Buchung. Die Reservierung weist einem oder mehreren Benutzern einen Teil des URL-Namespace zu. Mit diesem Vorgang haben Benutzer das Recht, sich für den angegebenen Namespace zu registrieren. Ein Benutzer, für den ein Namespace reserviert ist, wird als "eigener" Teil des URL-Namespace bezeichnet. Namespace Reservierungen werden in der Regel während der Installation der Anwendung ausgeführt und sind ein seltener Vorgang. Reservierungen bleiben bei Neustarts des Computers bestehen und erfordern Administratorrechte auf dem Computer oder den Besitz mit Delegierungs Berechtigungen zum Erstellen oder löschen.
-   Delegations. Delegierungs Berechtigungen ermöglichen einem Benutzer, der Besitzer eines Namespace ist, den Besitz einer Teilstruktur durch eine nachfolgende Reservierung an einen anderen Benutzer zu übergeben. Delegierungs Berechtigungen werden einem Benutzer vom Systemadministrator erteilt, wenn die Reservierung erfolgt. Einem Namespace können einem oder mehreren Benutzern Delegierungs Berechtigungen zugewiesen werden.

 

 




