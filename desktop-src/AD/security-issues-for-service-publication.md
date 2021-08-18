---
title: Sicherheitsprobleme bei der Dienstveröffentlichung
description: Das System schränkt die Möglichkeit ein, Verbindungspunktobjekte zu erstellen, zu ändern oder zu löschen. Beachten Und behandeln Sie diese Einschränkungen, wenn Sie einen Dienst veröffentlichen.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Sicherheitsprobleme bei Dienstveröffentlichungs-AD
- Active Directory, Using, Sicherheit, Sicherheitsprobleme bei der Dienstveröffentlichung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e4cec29d08a029bca52a99b573eb339964dd42274d3ca2e54795bb80b60897
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024908"
---
# <a name="security-issues-for-service-publication"></a>Sicherheitsprobleme bei der Dienstveröffentlichung

Das System schränkt die Möglichkeit ein, Verbindungspunktobjekte zu erstellen, zu ändern oder zu löschen. Beachten Und behandeln Sie diese Einschränkungen, wenn Sie einen Dienst veröffentlichen.

Clients müssen den in einem Verbindungspunktobjekt im Verzeichnis veröffentlichten Daten vertrauen können. Aus diesem Grund ist die Berechtigung zum Erstellen eines Verbindungspunktobjekts in der Regel auf privilegierte Benutzer wie Domänenadministratoren beschränkt. Dadurch wird verhindert, dass nicht autorisierte Benutzer Clients vertäussen, indem ungültige Verbindungspunkte für bekannte Dienste erstellt werden.

Dienste dürfen nicht mit Domänenadministratorberechtigungen ausgeführt werden. Dies bedeutet, dass ein Dienst in der Regel keinen eigenen Verbindungspunkt erstellen kann. Stattdessen stellen Sie eine Dienstinstallations- oder Konfigurationsanwendung zur Verfügung, die den Verbindungspunkt erstellt. Dieses Installationsprogramm muss von einem Benutzer mit den erforderlichen Berechtigungen ausgeführt werden.

Obwohl ein Dienst seinen Verbindungspunkt in der Regel nicht erstellen kann, muss er in der Lage sein, die Eigenschaften des Verbindungspunkts zur Laufzeit zu aktualisieren. Die Eigenschaften des Verbindungspunkts enthalten die Bindungsdaten, die von Clients zum Herstellen einer Verbindung mit dem Dienst verwendet werden. Wenn sich die Bindungsdaten ändern, muss der Dienst den Verbindungspunkt aktualisieren. Andernfalls können Clients den Dienst nicht verwenden. Dies bedeutet, dass das Installationsprogramm auch die Sicherheitsbeschreibung für das Verbindungspunktobjekt ändern muss, damit der Dienst die entsprechenden Eigenschaften zur Laufzeit lesen und schreiben kann. Weitere Informationen und ein Codebeispiel finden Sie unter [Aktivieren des Dienstkontos für den Zugriff auf SCP-Eigenschaften.](enabling-service-account-to-access-scp-properties.md)

Ein Dienst, der unter dem LocalSystem-Konto ausgeführt wird, kann einen Verbindungspunkt als untergeordnetes Objekt unter seinem eigenen Computerobjekt im Verzeichnis erstellen. Ein solcher Dienst ist eine Ausnahme von der Regel, dass Dienste keine eigenen Verbindungspunkte erstellen. Ein LocalSystem-Dienst verfügt auch über die Berechtigung, die Eigenschaften von Verbindungspunktobjekten unter seinem eigenen Computerobjekt zu ändern. Beachten Sie, dass ein Dienst nur unter dem LocalSystem-Konto ausgeführt werden sollte, wenn dies unbedingt erforderlich ist. Weitere Informationen finden Sie unter [Richtlinien für die Auswahl eines Dienstanmeldungskontos.](guidelines-for-selecting-a-service-logon-account.md)

Die Anwendung, die ein Verbindungspunktobjekt oder ein beliebiges Objekt erstellt, muss über untergeordnete Berechtigungen zum Erstellen der Objektklasse verfügen, die in dem Container erstellt werden soll, in dem das Objekt erstellt wird. Um ein Objekt zu entfernen, muss der Prozess, der den Vorgang ausführen, über untergeordnete Berechtigungen zum Löschen der Objektklasse verfügen, die für den Container gelöscht werden soll, der das Objekt enthält, oder über Löschberechtigungen für das Objekt selbst verfügen. Um einen Verbindungspunkt zu aktualisieren, muss der Prozess, der den Vorgang ausführen, über Schreibzugriff auf die Eigenschaften verfügen, die für das Objekt aktualisiert werden sollen.

 

 




