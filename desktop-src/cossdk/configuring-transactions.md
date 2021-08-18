---
description: Das Transaktionsattribut ist eine deklarative Eigenschaft, die Transaktionen für den Komponentenentwickler automatisch verwaltet. Durch Festlegen dieses Attributs entfällt die Notwendigkeit, explizite Transaktionssteuerelemente in Ihrer Komponente zu verwenden.
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: Konfigurieren von Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d613eb49a5f053b869e3efc90e04b9455644ea52acbaf651f33b00909e6e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128887"
---
# <a name="configuring-transactions"></a>Konfigurieren von Transaktionen

Das *Transaktionsattribut* ist eine deklarative Eigenschaft, die Transaktionen für den Komponentenentwickler automatisch verwaltet. Durch Festlegen dieses Attributs entfällt die Notwendigkeit, explizite Transaktionssteuerelemente in Ihrer Komponente zu verwenden.

COM+ verwendet das Transaktionsattribut der Komponente, um den Typ des Transaktionsschutzes zu bestimmen, der für jedes aktivierte Objekt erforderlich ist. Je nach Anforderung kann ein Objekt die Transaktion des Aufrufers freigeben, eine neue Transaktion erfordern oder ohne Transaktionsschutz arbeiten.

COM+ stellt die folgenden Transaktionsattributwerte zur Verfügung:

<dl> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Deaktiviert
</dt> <dd>

Im Allgemeinen sollten Sie diesen Attributwert nur festlegen, wenn Sie sicher sind, dass die Komponente nie auf einen Ressourcen-Manager zutritt. Wenn Sie das Transaktionsattribut deaktivieren, ignoriert COM+ die Transaktionsanforderungen der Komponente beim Bestimmen der Kontextplatzierung des Objekts. Daher kann das Objekt den Kontext (und die Transaktion) des Aufrufers freigeben. Wenn Sie eine COM-Komponente zu COM+ migrieren, müssen Sie das Transaktionsattribut deaktivieren, um das gleiche Transaktionsverhalten wie die nicht konfigurierte COM-Komponente zu erhalten.

> [!Note]  
> Eine *nicht konfigurierte Komponente ist* eine COM-Komponente, die nicht in einer COM+-Anwendung installiert wurde.

 

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>Nicht unterstützt
</dt> <dd>

Wenn Sie diesen Attributwert festlegen, stellt COM+ sicher, dass jedes aus der Komponente erstellte Objekt unabhängig vom Transaktionsstatus des Aufrufers nie an einer Transaktion beteiligt ist. Indem Sie diesen Wert deklarieren, stellen Sie sicher, dass ein Objekt nicht in der Transaktion des Aufrufers abstimmen kann und keine eigene Transaktion starten kann. Nicht unterstützt ist der Standardwert für alle Komponenten.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Unterstützt
</dt> <dd>

Wenn Sie diesen Attributwert festlegen, stellt COM+ sicher, dass alle aus der Komponente erstellten Objekte an einer Transaktion teilnehmen, sofern vorhanden. Sie deklarieren diesen Wert, wenn ein Objekt in der Transaktion des Aufrufers freigeben soll, ohne dass eine eigene Transaktion erforderlich ist.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Erforderlich
</dt> <dd>

Wenn Sie diesen Attributwert festlegen, stellt COM+ sicher, dass alle aus der Komponente erstellten Objekte transaktional sind. Wenn COM+ ein Objekt mit der Einstellung Erforderlich aktiviert, wird der Transaktionsstatus des Aufrufers untersucht. Wenn der Aufrufer über eine Transaktion verfügt, wird das neue -Objekt in die aktuelle Transaktion eingeschlossen. Andernfalls startet COM+ eine Transaktion, wodurch das neue Objekt zum Stamm der Transaktion wird. Dies ist die bevorzugte Einstellung für eine Komponente, die Ressourcenaktivitäten ausführt, da sie den Transaktionsschutz für diese Aktivitäten ermöglicht.

</dd> <dt>

<span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Erfordert Neu
</dt> <dd>

Wenn Sie diesen Attributwert festlegen, stellt COM+ sicher, dass alle von der Komponente erstellten Objekte an einer neuen Transaktion als Stamm der Transaktion teilnehmen müssen, unabhängig vom Transaktionsstatus des Aufrufers. COM+ initiiert automatisch eine neue Transaktion, die sich von der Transaktion des Aufrufers unterscheiden kann.

> [!Note]  
> COM+ unterstützt keine geschachtelten Transaktionen. Wenn ein Transaktionsobjekt eine andere Komponente aufruft, die als Neu erforderlich gekennzeichnet ist, erstellt COM+ eine unabhängige Transaktionsgrenze für das neu aktivierte Objekt. Die zweite Transaktion kann sich nicht auf die erste Transaktion auswirken, es sei denn, die erste Transaktion notiert explizit die Ergebnisse der zweiten Transaktion und ändert ihre Stimme basierend auf diesen Ergebnissen.

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a>Transaktionsattributabhängigkeiten

Die folgende Tabelle zeigt die Merkmale der einzelnen COM+-Transaktionsattributwerte, einschließlich der Auswirkungen des Werts auf Transaktionsmerkmale. COM+ erzwingt [die JIT-Aktivierung](com--just-in-time-activation.md) und [-Synchronisierung](com--synchronization.md) für alle Transaktionskomponenten.



| Attributwert          | Neue Transaktion   | Transaktion des Clients                 | Transaktionsstamm                        | JIT-Aktivierung      | Synchronisierung     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| Disabled<br/>      | Nie<br/>  | Vielleicht<br/>                     | Nie<br/>                        | Optional<br/> | Optional<br/> |
| Nicht unterstützt<br/> | Nie<br/>  | Nie<br/>                     | Nie<br/>                        | Optional<br/> | Optional<br/> |
| Unterstützt<br/>     | Nie<br/>  | Wenn der Client über eine Transaktion verfügt<br/> | Nie<br/>                        | Erforderlich<br/> | Erforderlich<br/> |
| Erforderlich<br/>      | Vielleicht<br/>  | Wenn der Client über eine Transaktion verfügt<br/> | Wenn der Client über keine Transaktion verfügt<br/> | Erforderlich<br/> | Erforderlich<br/> |
| Requires New<br/>  | Always<br/> | Nie<br/>                     | Always<br/>                       | Erforderlich<br/> | Erforderlich<br/> |



 

## <a name="transaction-boundaries"></a>Transaktionsgrenzen

Eine Transaktion hat einen Anfang, ein Ende und tritt genau einmal auf. Während der Ausführung kann eine Transaktion für eine Ressource, z. B. eine Datenbank oder Warteschlange, aufrufen, um eine oder mehrere Aufgaben auszuführen. Jede Ressource liegt innerhalb der *Transaktionsgrenze.* Alle Ressourcen innerhalb einer Transaktionsgrenze, die mehrere Prozess- und Computergrenzen umfassen kann, nutzen eine einzelne Transaktion gemeinsam. Die Verwaltung der Konsistenz zwischen diesen Prozess- und Computergrenzen ist wichtig.

COM+ sorgt für Konsistenz, indem Transaktionsgrenzen basierend auf dem Wert des Transaktionsattributs, das Sie für jede Komponente festlegen, automatisch verwalten. Eine COM+-Transaktion fließt automatisch an Objekte, die angewiesen sind, an einer Transaktion teilzunehmen, und umgeht Objekte, die außerhalb einer Transaktion ausgeführt werden. COM+ unterstützt keine geschachtelten Transaktionen. Stattdessen sind COM+-Transaktionen eindeutig und kurzlebig.

Das erste Objekt in einer Transaktionsgrenze ist speziell für die Transaktion und wird als *Stammobjekt der* Transaktion bezeichnet. Es kann nur ein Stammobjekt in einer Transaktion geben. Alle anderen Objekte in der Transaktionshierarchie unter dem Stammobjekt werden als *innere Objekte bezeichnet.*

## <a name="mapping-transactions"></a>Zuordnen von Transaktionen

Eine Möglichkeit, sicherzustellen, dass ein Objekt in der richtigen Transaktionsgrenze enthalten ist, besteht darin, Ihre Transaktionen zu zuordnen, bevor Sie mit dem Schreiben ihrer Komponenten beginnen. Indem Sie Transaktionen zuordnen, können Sie die beste Einstellung für jede Komponente bestimmen, die Sie schreiben. Wenn Sie sicher sind, wie Ihre Komponenten verwendet werden sollen, desto einfacher ist es, den richtigen Transaktionsattributwert auszuwählen.

Zur Laufzeit untersucht COM+ das Transaktionsattribut, um zu bestimmen, ob ein Objekt der Stamm einer neuen Transaktion sein, in einer vorhandenen Transaktion erstellt oder als nicht transaktionales Objekt erstellt werden soll.

Die folgende Abbildung zeigt eine mögliche Transaktionszuordnung. In der Abbildung erstellt der Client Objekt 1, das eine Transaktion erfordert. Da keine Transaktion vorhanden ist, erstellt COM+ Transaktion 1 und platziert Objekt 1 als Stammobjekt. Objekt 1 erstellt Objekt 2, das Transaktionen unterstützt und daher in Transaktion 1 platziert wird. Objekt 2 erstellt Objekt 3, das keine Transaktionen unterstützt und daher außerhalb aller Transaktionen platziert wird. Objekt 2 erstellt auch Objekt 4, das eine Transaktion erfordert und daher in Transaktion 1 platziert wird. Objekt 3 erstellt Objekt 5, das Transaktionen unterstützt. Da Objekt 5 jedoch von einem Objekt erstellt wird, das in einer Transaktion nicht vorhanden ist, wird es auch außerhalb aller Transaktionen platziert. Objekt 4 erstellt Objekt 6, das eine neue Transaktion erfordert, sodass COM+ Transaktion 2 erstellt und Objekt 6 als Stammobjekt platziert. Objekt 6 erstellt Objekt 7, das Transaktionen unterstützt und daher in Transaktion 2 platziert wird.

![Diagramm, das eine Clientinteraktion mit Transaktion 1 und Transaktion 2 zeigt.](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

Die obige Abbildung zeigt zwei potenzielle Problembereiche. Erstens wird der Großteil der Arbeit auf zwei unterschiedliche Transaktionen aufgeteilt. Wenn Transaktion 1 fehlschlägt, nachdem Objekt 4 Objekt 6 erstellt hat, wird Transaktion 2 ausgeführt, ohne vom Ergebnis von Transaktion 1 betroffen zu sein. Wenn dieses Ergebnis unbeabsichtigt ist, sollten Sie die Vorgänge beider Transaktionen in eine einzelne Transaktion aufklappen, was Sie erreichen können, indem Sie das Transaktionsattribut von Objekt 6 in Erforderlich ändern.

Die Zuordnungsabbildung zeigt auch, dass Objekt 3 und Objekt 5 nicht transaktional sind und vollständig außerhalb des Bereichs von Transaktionen 1 und 2 ausgeführt werden. Wenn Objekt 5 persistente Daten aktualisiert, sollten Sie deren nicht transaktionalen Status überprüfen. Objekt 5 kann innerhalb einer Transaktion platziert werden, indem sein Transaktionsattribut in Erforderlich geändert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen des Transaktionsattributs](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




