---
title: Verteiltes Dateisystem (DFS)-Funktionen
description: Die verteiltes Dateisystem (DFS)-Funktionen bieten die Möglichkeit, Freigaben auf mehreren Servern logisch zu gruppieren und Freigaben in einem einzelnen hierarchischen Namespace transparent zu verknüpfen. DFS organisiert freigegebene Ressourcen in einem Netzwerk in einer Struktur ähnliches-Struktur.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73738d4f503d10e7668f0f323583f49604e3a90d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214258"
---
# <a name="distributed-file-system-dfs-functions"></a>Verteiltes Dateisystem (DFS)-Funktionen

Die verteiltes Dateisystem (DFS)-Funktionen bieten die Möglichkeit, Freigaben auf mehreren Servern logisch zu gruppieren und Freigaben in einem einzelnen hierarchischen Namespace transparent zu verknüpfen. DFS organisiert freigegebene Ressourcen in einem Netzwerk in einer Struktur ähnliches-Struktur.

DFS unterstützt *eigenständige* DFS-Namespaces, die mit einem Host Server und *domänenbasierten* Namespaces mit mehreren Host Servern und Hochverfügbarkeit. Die DFS- *Topologiedaten* für Domänen basierte Namespaces werden in Active Directory gespeichert. Die Daten umfassen den DFS-Stamm, DFS-Links und DFS-Ziele.

Jede DFS-Struktur verfügt über ein oder mehrere Stamm *Ziele*. Das Stammziel ist ein Host Server, auf dem der DFS-Dienst ausgeführt wird. Eine DFS-Struktur kann eine oder mehrere *DFS-Links* enthalten. Jeder DFS-Link verweist auf mindestens einen freigegebenen Ordner im Netzwerk. Sie können DFS-Links aus einem DFS-Namespace hinzufügen, ändern und löschen. Wenn Sie das letzte Ziel entfernen, das einer DFS-Verknüpfung zugeordnet ist, löscht DFS den DFS-Link im DFS-Namespace. (In der früheren Dokumentation wurden DFS-Links als Verknüpfungs Punkte bezeichnet.)

Ein DFS-Link kann auf einen oder mehrere freigegebene Ordner verweisen. die Ordner werden als *Ziele* bezeichnet. Wenn Benutzer auf einen DFS-Link zugreifen, wählt der DFS-Server basierend auf den Standortinformationen eines Clients eine Gruppe von Zielen aus. Der Client greift auf das erste verfügbare Ziel in der Gruppe zu. Dies hilft bei der Verteilung von Client Anforderungen auf die möglichen Ziele und kann auch dann weiterhin für Benutzer sorgen, wenn einige Server ausfallen.

Eine Anwendung kann die DFS-Funktionen für Folgendes verwenden:

- Fügen Sie einem DFS-Stamm einen DFS-Link hinzu.
- Erstellen oder entfernen Sie eigenständige und Domänen basierte DFS-Namespaces.
- Fügen Sie einem vorhandenen DFS-Link Ziele hinzu.
- Entfernen Sie eine DFS-Verknüpfung aus einem DFS-Stamm.
- Entfernen Sie ein Ziel aus einem DFS-Link.
- Informationen zu DFS-Stamm Elementen und Links anzeigen und konfigurieren.

Eine Liste der DFS-Funktionen finden Sie unter [verteiltes Dateisystem Functions](distributed-file-system-functions.md).

Eine Liste der DFS-Strukturen finden Sie unter [verteiltes Dateisystem Strukturen](distributed-file-system-structures.md).

Ziele auf Computern, auf denen Microsoft Windows ausgeführt wird, können in einem DFS-Namespace veröffentlicht werden. Sie können auch alle nicht-Microsoft-Freigaben veröffentlichen, für die clientredirectors in einem DFS-Namespace verfügbar sind. Anders als bei einer Freigabe, die auf einem Server veröffentlicht wird, auf dem Windows Server ausgeführt wird, können Sie jedoch keinen DFS-Stamm hosten oder Verweise auf andere DFS-Ziele bereitstellen.

DFS verwendet den Windows Server-Datei Replikations Dienst zum Kopieren von Änderungen zwischen replizierten Zielen. Benutzer können Dateien ändern, die auf einem Ziel gespeichert sind, und der Datei Replikations Dienst gibt die Änderungen an die anderen vorgesehenen Ziele weiter. Der Dienst behält die neuesten Änderungen an einem Dokument oder an Dateien bei.
