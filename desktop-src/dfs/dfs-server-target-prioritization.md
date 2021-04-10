---
title: Priorisierung des DFS-Server Ziels
description: Die Priorisierung des DFS-Server Ziels ist ein Feature, das in Microsoft Windows Server 2003 mit Service Pack 1 (SP1) und späteren Betriebssystemen verfügbar ist.
ms.assetid: 0aacebf7-49cc-4287-a5c4-0d25a416d227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e784a540a67f624ca5b8075009cd862c6063427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214278"
---
# <a name="dfs-server-target-prioritization"></a>Priorisierung des DFS-Server Ziels

Die Priorisierung des DFS-Server Ziels ist ein Feature, das in Microsoft Windows Server 2003 mit Service Pack 1 (SP1) und späteren Betriebssystemen verfügbar ist. Mit diesem Feature können DFS-Server die verfügbaren Active Directory Standortkosten Informationen nutzen, um die Ziele in den Client verweisen zu priorisieren.

Vor Windows Server 2003 mit SP1 wurden Ziele in zwei Gruppen unterteilt: eine Gruppe, die alle Ziele an demselben Standort wie der Client enthält. und eine weitere Gruppe für alle anderen Ziele. Die Ziele, die dieselbe Website wie der Client gemeinsam nutzen, werden als "in-Site" bezeichnet, und wenn Standortkosten aktiviert ist, wird Ihnen ein spezifischer Kosten Wert in Relation zum Gesamt Standort zugewiesen, wobei niedrigere Standortkosten als höher bevorzugt werden.

Mit der Verfügbarkeit dieser Standortkosten Daten können Server Ziele für effektivere DFS-Server-failoverstrategien priorisiert werden. In der Vergangenheit war dieser detaillierte Detailgrad nicht verfügbar, und Administratoren mussten auf künstliche Mittel (z. b. dummysites in AD) zurückgreifen, um auch einfache Anforderungen zu unterstützen, wie z. b. die Bezeichnung bestimmter Server als "Sicherungs-" oder "sekundärer" Server, wenn ein "primärer DFS-Server ausfällt. Mit den zusätzlichen Details der Site-Kosten sind nun mehrstufige failoverstrategien möglich.

In der folgenden Erläuterung wird davon ausgegangen, dass die Standortkosten aktiviert ist.

## <a name="target-prioritization"></a>Ziel Priorisierung

Die Ziel Priorität ist eine bestimmte Reihenfolge aus administrativer Sicht und die Klassifizierung und Rangfolge von Standort Servern in der expliziten Einstellung basierend auf Ihren Standortkosten von einem DFS-Client. Die globale Priorität ist unabhängig von den Standortkosten. Beachten Sie, dass globale Prioritäts Klassen nicht notwendigerweise die optimalen Ziele aus der Perspektive eines DFS-Clients angeben, sondern die Wichtigkeit oder fehlende Wichtigkeit bestimmter Ziele aus der Perspektive eines Website Administrators widerspiegeln.

Die Server Ziel Priorität ist in zwei Kategorien unterteilt: Prioritäts Klasse und Prioritäts Rang. Prioritäts Klassen werden in zwei Ebenen unterteilt: lokal und Global. Innerhalb dieser Klassen gibt es eine grobe Reihenfolge von Zielen, die auf den Standortkosten basieren und als hoch, normal und mit niedriger Priorität gruppiert sind. Das Ergebnis sind fünf Prioritäts Klassen, von der höchsten zur niedrigsten Priorität wie folgt:

- Globale hohe Priorität
- Site-Kosten hohe Priorität
- Standort-Kosten normale Priorität
- Standort-Kosten niedrige Priorität
- Globale niedrige Priorität

Die Standortkosten Klassen können als Unterbereiche der "globalen normalen Priorität" betrachtet werden. Der Prioritäts Rang ist eine einfache ganzzahlige Rangfolge auf der Grundlage von Ordinalwerten: 0, 1, 2 und weiter, wobei 0 der höchste Wert und alle nachfolgenden Werte den absteigenden Rang angibt.

Die globalen High-und Low-Prioritäten werden keine Standortkosten Werte in Erwägung gezogen. Ziele mit globaler Priorität mit hoher Priorität werden für alle anderen Ziele übernommen, und Ziele mit einer globalen niedrigen Priorität erhalten die geringste Priorität.

Beim Bestellen eines Verweises umfasst der gesamte Prozess die folgenden Schritte:

1. Die Sätze globaler High-und Low-Ziele werden zusammen mit den verbleibenden "globalen normalen" Zielen identifiziert.
2. Wenn die Option "Insite" festgelegt ist, werden alle Ziele außerhalb des Client Standorts entfernt. Die Option "Insite" wird nicht auf die globalen Sätze mit hoher und niedriger Priorität angewendet.
3. Innerhalb dieser drei Sätze werden die Ziele mithilfe des AD-Standortkosten Mechanismus geordnet, wobei entweder eine lokale oder eine vollständige Website Kosten verwendet werden. Das Ergebnis sind Sätze von Zielen gleicher Standortkosten.
4. Innerhalb der Sätze von "globalen normalen" Zielen gleicher Standortkosten wird den Zielen eine Prioritäts Klasse aus den Rang folgen Kosten für hohe, normale und niedrige Priorität zugewiesen.
5. Innerhalb der Sätze von Zielen gleicher Standortkosten und Prioritäts Klasse werden Ziele nun nach Prioritäts Rang geordnet, wobei 0 der höchste Rang ist.
6. Innerhalb der Ziele gleicher Standortkosten, Prioritäts Klasse und Prioritäts Rang werden Ziele für den Lastenausgleich nach dem Zufallsprinzip gemischt.

Grafisch gesehen wird ein Satz von Zielen wie folgt angeordnet:

- globale Ziele mit hoher Priorität 
- Site-Cost Class Targets mit hoher Priorität mit Standortkosten = 0
- normal mit Standortkosten = 0
- niedrig mit Standortkosten = 0
- Site-Cost Class Targets mit hoher Priorität mit Standortkosten = 1
- normal mit Standortkosten = 1
- niedrig mit Standortkosten = 1
- Durchführen weiterer Operationen
- globale Ziel Klassenziele mit niedriger Priorität

Innerhalb dieser Sätze werden Ziele nach Prioritäts Rang sortiert. Der höchste Rang ist 0 (null), wobei jeder nachfolgende ganzzahlige Wert (1, 2 usw.) einen immer niedrigeren Rang angibt.

Die Ziel Priorität wird für ein bestimmtes Ziel einer Verknüpfung (oder eines Stamms) in einem DFS-Namespace festgelegt. Die Priorität eines Ziels für einen Link wirkt sich nicht auf die Anordnung anderer Links aus, wenn derselbe Zielpfad mehrmals verwendet wird. Wenn beispielsweise zwei Verknüpfungen \\ \\ Server \\ share1 als Ziel haben, wird die Priorität von \\ \\ Server \\ share1 für beide Verknüpfungen separat festgelegt.

Die Standardpriorität für alle Links ist die Site-Cost Normal Priorität mit dem Rang 0. Die Ziel Priorität wirkt sich nicht auf die Reihenfolge der Verweise aus, es sei denn, Sie wird verwendet, und alle vorhandenen Links werden nach dem Empfang geordnet.

Die Verweis Antwort von einem DFS-Server besteht aus Zielsätzen, wie oben angegeben, wobei jeder nicht globale Zielsatz Ziele mit den gleichen Standortkosten, der Prioritäts Klasse und dem Prioritäts Rang enthält. Ziele innerhalb der einzelnen Sätze werden nach dem Zufallsprinzip geordnet. DFS-Clients, die den Verweis erhalten, beginnen mit dem ersten Ziel der ersten Gruppe und durchlaufen die Liste, bis ein verfügbares Ziel für einen bestimmten DFS-Stamm oder-Link gefunden wird.

Die spezifische API-Implementierung dieses Features finden Sie in den folgenden Referenz Themen:

[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6) 
 [**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104) 
 [**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106) 
 [**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority) 
 [**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)
