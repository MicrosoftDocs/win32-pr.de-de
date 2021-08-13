---
title: dfs-Funktionen (verteiltes Dateisystem)
description: Die dfs-Funktionen (verteiltes Dateisystem) bieten die Möglichkeit, Freigaben logisch auf mehreren Servern zu gruppieren und Freigaben transparent mit einem einzelnen hierarchischen Namespace zu verknüpfen. DFS organisiert freigegebene Ressourcen in einem Netzwerk in einer strukturähnlichen Struktur.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898d44ecfaeb99145570230e49156440dc9e2aac02051baa47bb496a0f58b2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380580"
---
# <a name="distributed-file-system-dfs-functions"></a>dfs-Funktionen (verteiltes Dateisystem)

Die dfs-Funktionen (verteiltes Dateisystem) bieten die Möglichkeit, Freigaben logisch auf mehreren Servern zu gruppieren und Freigaben transparent mit einem einzelnen hierarchischen Namespace zu verknüpfen. DFS organisiert freigegebene Ressourcen in einem Netzwerk in einer strukturähnlichen Struktur.

DFS unterstützt *eigenständige DFS-Namespaces,* solche mit einem Hostserver und *domänenbasierte* Namespaces mit mehreren Hostservern und Hochverfügbarkeit. Die *DFS-Topologiedaten* für domänenbasierte Namespaces werden in Active Directory gespeichert. Die Daten umfassen den DFS-Stamm, DFS-Links und DFS-Ziele.

Jede DFS-Struktur verfügt über mindestens ein *Stammziel.* Das Stammziel ist ein Hostserver, auf dem der DFS-Dienst ausgeführt wird. Eine DFS-Struktur kann mindestens einen *DFS-Link* enthalten. Jeder DFS-Link verweist auf einen oder mehrere freigegebene Ordner im Netzwerk. Sie können DFS-Links aus einem DFS-Namespace hinzufügen, ändern und löschen. Wenn Sie das letzte Ziel entfernen, das einem DFS-Link zugeordnet ist, löscht DFS den DFS-Link im DFS-Namespace. (In der vorherigen Dokumentation wurden DFS-Links als Verbindungspunkt bezeichnet.)

Ein DFS-Link kann auf einen oder mehrere freigegebene Ordner verweisen. Die Ordner werden als *Ziele* bezeichnet. Wenn Benutzer auf einen DFS-Link zugreifen, wählt der DFS-Server basierend auf den Standortinformationen eines Clients eine Gruppe von Zielen aus. Der Client greift auf das erste verfügbare Ziel in der Gruppe zu. Dies hilft bei der Verteilung von Clientanforderungen auf die möglichen Ziele und kann benutzern auch dann weiterhin Zugriff bieten, wenn einige Server ausfallen.

Eine Anwendung kann die DFS-Funktionen für Folgendes verwenden:

- Fügen Sie einem DFS-Stamm einen DFS-Link hinzu.
- Erstellen oder Entfernen eigenständiger und domänenbasierter DFS-Namespaces.
- Fügen Sie einem vorhandenen DFS-Link Ziele hinzu.
- Entfernen sie einen DFS-Link aus einem DFS-Stamm.
- Entfernen eines Ziels aus einem DFS-Link.
- Anzeigen und Konfigurieren von Informationen zu DFS-Stämmen und Links.

Eine Liste der DFS-Funktionen finden Sie unter [verteiltes Dateisystem Functions](distributed-file-system-functions.md).

Eine Liste der DFS-Strukturen finden Sie unter [verteiltes Dateisystem Strukturen.](distributed-file-system-structures.md)

Ziele auf Computern, auf denen Microsoft Windows ausgeführt wird, können in einem DFS-Namespace veröffentlicht werden. Sie können auch alle Nicht-Microsoft-Freigaben veröffentlichen, für die Clientumleitungsoren in einem DFS-Namespace verfügbar sind. Im Gegensatz zu einer Freigabe, die auf einem Server veröffentlicht wird, auf dem Windows Server ausgeführt wird, können sie jedoch keinen DFS-Stamm hosten oder Verweise auf andere DFS-Ziele bereitstellen.

DFS verwendet den Windows Server-Dateireplikationsdienst, um Änderungen zwischen replizierten Zielen zu kopieren. Benutzer können Dateien ändern, die auf einem Ziel gespeichert sind, und der Dateireplikationsdienst gibt die Änderungen an die anderen festgelegten Ziele weiter. Der Dienst behält die letzte Änderung an einem Dokument oder einer Datei bei.
