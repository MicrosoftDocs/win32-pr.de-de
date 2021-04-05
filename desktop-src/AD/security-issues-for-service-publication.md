---
title: Sicherheitsprobleme bei der Dienst Veröffentlichung
description: Das System schränkt die Fähigkeit ein, Verbindungspunkt Objekte zu erstellen, zu ändern oder zu löschen. Beachten Sie diese Einschränkungen, und behandeln Sie diese, wenn Sie einen Dienst veröffentlichen.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Sicherheitsprobleme bei der Dienst Veröffentlichungs Anzeige
- Active Directory, Verwendung, Sicherheit, Sicherheitsprobleme bei der Dienst Veröffentlichung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee5be89c490fa938cdc9c7cf3d7d72434a3dffa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707553"
---
# <a name="security-issues-for-service-publication"></a>Sicherheitsprobleme bei der Dienst Veröffentlichung

Das System schränkt die Fähigkeit ein, Verbindungspunkt Objekte zu erstellen, zu ändern oder zu löschen. Beachten Sie diese Einschränkungen, und behandeln Sie diese, wenn Sie einen Dienst veröffentlichen.

Clients müssen in der Lage sein, den Daten, die in einem Verbindungspunkt Objekt im Verzeichnis veröffentlicht werden, zu vertrauen. Aus diesem Grund ist die Berechtigung zum Erstellen eines Verbindungspunkt Objekts in der Regel auf privilegierte Benutzer (z. b. Domänen Administratoren) beschränkt. Dadurch wird verhindert, dass nicht autorisierte Benutzer Clients täuschen, indem ungültige Verbindungspunkte für bekannte Dienste erstellt werden.

Dienste dürfen nicht mit Domänen Administratorrechten ausgeführt werden. Dies bedeutet, dass ein Dienst in der Regel keinen eigenen Verbindungspunkt erstellen kann. Stattdessen stellen Sie eine Dienst Installation oder eine Konfigurationsanwendung bereit, die den Verbindungspunkt erstellt. Dieser Installer muss von einem Benutzer mit den erforderlichen Berechtigungen ausgeführt werden.

Obwohl ein Dienst den Verbindungspunkt in der Regel nicht erstellen kann, muss er die Verbindungspunkt Eigenschaften zur Laufzeit aktualisieren können. Die Verbindungspunkt Eigenschaften enthalten die Bindungs Daten, die von Clients zum Herstellen einer Verbindung mit dem Dienst verwendet werden. Wenn sich die Bindungs Daten ändern, muss der Dienst den Verbindungspunkt aktualisieren. Andernfalls können Clients den Dienst nicht verwenden. Dies bedeutet, dass das Installationsprogramm auch die Sicherheits Beschreibung für das Verbindungspunkt Objekt ändern muss, damit der Dienst die entsprechenden Eigenschaften zur Laufzeit lesen und schreiben kann. Weitere Informationen und ein Codebeispiel finden Sie unter [Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften](enabling-service-account-to-access-scp-properties.md).

Ein Dienst, der unter dem Konto "LocalSystem" ausgeführt wird, kann einen Verbindungspunkt als untergeordnetes Objekt unter dem eigenen Computer Objekt im Verzeichnis erstellen. Ein solcher Dienst stellt eine Ausnahme von der Regel dar, bei der Dienste keine eigenen Verbindungspunkte erstellen. Ein LocalSystem-Dienst verfügt auch über die Berechtigung zum Ändern der Eigenschaften von Verbindungspunkt Objekten unter seinem eigenen Computer Objekt. Beachten Sie, dass ein Dienst nur dann unter dem Konto LocalSystem ausgeführt werden sollte, wenn dies unbedingt erforderlich ist. Weitere Informationen finden Sie unter [Richtlinien für die Auswahl eines Dienst Anmelde Kontos](guidelines-for-selecting-a-service-logon-account.md).

Die Anwendung, die ein Verbindungspunkt Objekt erstellt, oder ein beliebiges-Objekt muss über die Berechtigung untergeordnete Berechtigungen erstellen für die Objektklasse verfügen, die im Container erstellt werden soll, in dem das Objekt erstellt wird. Um ein Objekt zu entfernen, muss der Prozess, der den Vorgang ausführt, über untergeordnete Berechtigungen löschen verfügen, damit die Objektklasse für den Container gelöscht werden kann, der das Objekt enthält, oder über Lösch Berechtigungen für das Objekt selbst verfügen. Zum Aktualisieren eines Verbindungs Punkts muss der Prozess, der den Vorgang ausführt, über Schreibzugriff auf die für das Objekt zu aktualisierenden Eigenschaften verfügen.

 

 




