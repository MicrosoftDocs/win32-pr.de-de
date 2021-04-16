---
description: Das Transaction-Attribut ist eine deklarative Eigenschaft, die Transaktionen für den Komponenten Entwickler automatisch verwaltet. Durch Festlegen dieses Attributs entfällt die Notwendigkeit, explizite Transaktionssteuer Elemente in der Komponente zu verwenden.
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: Konfigurieren von Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57f27d47836193dc5d23c44e3344cb2a81d5984
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104562750"
---
# <a name="configuring-transactions"></a>Konfigurieren von Transaktionen

Das *Transaction-Attribut* ist eine deklarative Eigenschaft, die Transaktionen für den Komponenten Entwickler automatisch verwaltet. Durch Festlegen dieses Attributs entfällt die Notwendigkeit, explizite Transaktionssteuer Elemente in der Komponente zu verwenden.

Com+ verwendet das Transaktions Attribut der Komponente, um den Typ des Transaktions Schutzes zu ermitteln, der für jedes aktivierter Objekt erforderlich ist. Abhängig von der Anforderung kann ein Objekt die Transaktion des Aufrufers freigeben, eine neue Transaktion anfordern oder ohne Transaktions Schutz arbeiten.

Com+ bietet die folgenden Transaktions Attributwerte:

<dl> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Deaktiviert
</dt> <dd>

Im Allgemeinen sollten Sie diesen Attribut Wert nur festlegen, wenn Sie sicher sind, dass die Komponente niemals auf einen Ressourcen-Manager zugreift. Wenn Sie das Transaktions Attribut deaktivieren, ignoriert com+ die Transaktions Anforderungen der Komponente bei der Bestimmung der Kontext Platzierung des Objekts. Folglich kann das Objekt den Kontext (und die Transaktion) seines Aufrufers freigeben. Wenn Sie eine COM-Komponente zu com+ migrieren, müssen Sie das Transaktions Attribut deaktivieren, damit das gleiche Transaktionsverhalten wie die nicht konfigurierte COM-Komponente erhalten bleibt.

> [!Note]  
> Eine nicht *konfigurierte Komponente* ist eine COM-Komponente, die nicht in einer COM+-Anwendung installiert wurde.

 

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>Nicht unterstützt
</dt> <dd>

Wenn Sie diesen Attribut Wert festlegen, stellt com+ sicher, dass jedes von der Komponente erstellte Objekt nie an einer Transaktion teilnimmt, unabhängig vom Transaktionsstatus seines Aufrufers. Wenn Sie diesen Wert deklarieren, stellen Sie sicher, dass ein Objekt nicht in der Transaktion des Aufrufers Stimmen und keine eigene Transaktion starten kann. Nicht unterstützt ist der Standardwert für alle Komponenten.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Unterstützt
</dt> <dd>

Wenn Sie diesen Attribut Wert festlegen, stellt com+ sicher, dass jedes von der Komponente erstellte Objekt an einer Transaktion teilnimmt, wenn eine solche vorhanden ist. Sie deklarieren diesen Wert, wenn ein Objekt in der Transaktion des Aufrufers freigegeben werden soll, ohne dass eine eigene Transaktion erforderlich ist.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Erforderlich
</dt> <dd>

Wenn Sie diesen Attribut Wert festlegen, stellt com+ sicher, dass jedes von der Komponente erstellte Objekt transaktional ist. Wenn com+ ein Objekt mit der erforderlichen Einstellung aktiviert, prüft es den Transaktionsstatus des Aufrufers. Wenn der Aufrufer über eine Transaktion verfügt, ist das neue-Objekt in der aktuellen Transaktion enthalten. Andernfalls startet com+ eine Transaktion, sodass das neue Objekt zum Stamm der Transaktion wird. Dies ist die bevorzugte Einstellung für eine Komponente, die Ressourcen Aktivitäten ausführt, da Sie den Transaktions Schutz für diese Aktivitäten bereitstellt.

</dd> <dt>

<span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Erfordert neu
</dt> <dd>

Wenn Sie diesen Attribut Wert festlegen, stellt com+ sicher, dass alle Objekte, die von der Komponente erstellt werden, an einer neuen Transaktion als Stamm der Transaktion teilnehmen müssen, unabhängig vom Transaktionsstatus des Aufrufers. Com+ initiiert automatisch eine neue Transaktion, die sich von der Transaktion des Aufrufers unterscheidet.

> [!Note]  
> Com+ unterstützt keine netsted Transactions. Wenn ein Transaktions Objekt eine andere Komponente aufruft, die als erforderlich markiert ist, erstellt com+ eine unabhängige transaktionale Grenze für das neu aktivierte Objekt. Die zweite Transaktion kann die erste Transaktion nicht beeinflussen, es sei denn, die erste Transaktion notiert explizit die Ergebnisse der zweiten Transaktion und ändert Ihre Stimme auf der Grundlage dieser Ergebnisse.

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a>Transaktions Attribut Abhängigkeiten

In der folgenden Tabelle werden die Merkmale der einzelnen com+-Transaktions Attributwerte angezeigt, einschließlich der Auswirkung des Werts auf die Transaktionseigenschaften. Com+ erzwingt die [JIT-Aktivierung](com--just-in-time-activation.md) und- [Synchronisierung](com--synchronization.md) für alle Transaktions Komponenten.



| Attributwert          | Neue Transaktion   | Client Transaktion                 | Transaktions Stamm                        | JIT-Aktivierung      | Synchronization     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| Disabled<br/>      | Nie<br/>  | Vielleicht<br/>                     | Nie<br/>                        | Optional<br/> | Optional<br/> |
| Nicht unterstützt<br/> | Nie<br/>  | Nie<br/>                     | Nie<br/>                        | Optional<br/> | Optional<br/> |
| Unterstützt<br/>     | Nie<br/>  | Wenn der Client über eine Transaktion verfügt<br/> | Nie<br/>                        | Erforderlich<br/> | Erforderlich<br/> |
| Erforderlich<br/>      | Vielleicht<br/>  | Wenn der Client über eine Transaktion verfügt<br/> | Wenn der Client keine Transaktion hat<br/> | Erforderlich<br/> | Erforderlich<br/> |
| Requires New<br/>  | Always<br/> | Nie<br/>                     | Always<br/>                       | Erforderlich<br/> | Erforderlich<br/> |



 

## <a name="transaction-boundaries"></a>Transaktionsgrenzen

Eine Transaktion verfügt über einen Anfang, ein Ende und tritt genau einmal auf. Während der Ausführung kann eine Transaktion für eine Ressource, z. b. eine Datenbank oder Warteschlange, Aufrufe ausführen, um eine oder mehrere Tasks auszuführen. Jede Ressource fällt in die *Transaktionsgrenze*. Alle Ressourcen innerhalb einer Transaktionsgrenze, die mehrere Prozess-und Computer Grenzen umfassen können, haben eine einzelne Transaktion gemeinsam. Die Verwaltung von Konsistenz über diese Prozess-und Computer Grenzen hinweg ist wichtig.

Com+ gewährleistet die Konsistenz durch die automatische Verwaltung der Transaktionsgrenzen, basierend auf dem Wert des Transaktions Attributs, das Sie für die einzelnen Komponenten festgelegt haben. Eine COM+-Transaktion fließt automatisch zu den Objekten, die für die Teilnahme an einer Transaktion angewiesen sind, und umgeht Objekte, die außerhalb einer Transaktion ausgeführt werden. Com+ unterstützt keine netsted Transactions. Stattdessen sind com+-Transaktionen eindeutig und kurzlebig.

Das erste Objekt in einer Transaktionsgrenze ist für die Transaktion spezifisch und wird als Stamm *Objekt* der Transaktion bezeichnet. Es darf nur ein Stamm Objekt in einer Transaktion vorhanden sein. Alle anderen Objekte in der transaktionalen Hierarchie unter dem Root-Objekt werden als *innere Objekte* bezeichnet.

## <a name="mapping-transactions"></a>Zuordnung von Transaktionen

Eine Möglichkeit, um sicherzustellen, dass ein Objekt in der richtigen Transaktionsgrenze enthalten ist, ist das Zuordnen der Transaktionen, bevor Sie mit dem Schreiben der Komponenten beginnen. Durch die Zuordnung von Transaktionen können Sie die beste Einstellung für jede Komponente ermitteln, die Sie schreiben. Wenn Sie mehr darüber erfahren, wie Ihre Komponenten verwendet werden sollen, desto einfacher ist es, den richtigen Transaktions Attribut Wert auszuwählen.

Zur Laufzeit prüft com+ das Transaction-Attribut, um zu bestimmen, ob ein Objekt der Stamm einer neuen Transaktion, in einer vorhandenen Transaktion erstellt oder als nicht transaktionales Objekt erstellt werden soll.

Die folgende Abbildung zeigt eine mögliche Transaktions Zuordnung. In der Abbildung erstellt der Client das Objekt 1, für das eine Transaktion erforderlich ist. Da keine Transaktion vorhanden ist, erstellt COM+ Transaktion 1 und platziert Objekt 1 darin als Stamm Objekt. Objekt 1 erstellt Objekt 2, das Transaktionen unterstützt und daher in Transaktion 1 platziert wird. Objekt 2 erstellt Objekt 3, das keine Transaktionen unterstützt und daher außerhalb aller Transaktionen platziert wird. Objekt 2 erstellt außerdem das Objekt 4, das eine Transaktion erfordert und daher in Transaktion 1 platziert wird. Objekt 3 erstellt Objekt 5, das Transaktionen unterstützt. Da Objekt 5 jedoch von einem Objekt erstellt wird, das in einer Transaktion nicht vorhanden ist, wird es auch außerhalb aller Transaktionen platziert. Objekt 4 erstellt Objekt 6, das eine neue Transaktion erfordert, sodass COM+ Transaktion 2 erstellt und Objekt 6 darin als Stamm Objekt platziert. Objekt 6 erstellt das Objekt 7, das Transaktionen unterstützt und daher in Transaktion 2 platziert wird.

![Diagramm, das eine Client Interaktion mit Transaktion 1 und Transaktion 2 zeigt.](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

Die obige Abbildung zeigt zwei mögliche Problembereiche. Zuerst wird der Großteil der Arbeit zwischen zwei unterschiedlichen Transaktionen aufgeteilt. Wenn Transaktion 1 fehlschlägt, nachdem Objekt 4 Objekt 6 erstellt hat, wird Transaktion 2 durch das Ergebnis von Transaktion 1 nicht beeinträchtigt. Wenn dieses Ergebnis unbeabsichtigt ist, können Sie die Vorgänge beider Transaktionen in einer einzigen Transaktion durchführen, indem Sie das Transaktions Attribut von Objekt 6 in erforderlich ändern.

Die Mapping-Abbildung zeigt auch, dass Objekt 3 und Objekt 5 nicht transaktional sind und vollständig außerhalb des Bereichs der Transaktionen 1 und 2 ausgeführt werden. Wenn Objekt 5 persistente Daten aktualisiert, empfiehlt es sich, den nicht transaktionalen Status zu überdenken. Objekt 5 kann in eine Transaktion eingefügt werden, indem das Transaktions Attribut in required geändert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen des Transaktions Attributs](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




