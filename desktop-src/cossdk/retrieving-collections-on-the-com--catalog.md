---
description: Abrufen von Auflistungen im com+-Katalog
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Abrufen von Auflistungen im com+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748032"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Abrufen von Auflistungen im com+-Katalog

Daten im com+-Katalog werden in einer Hierarchie von Sammlungen gespeichert. Im Verwaltungs Programmkomponenten Dienste werden viele dieser Sammlungen als Ordner in der Konsolen Struktur angezeigt. Sammlungen, die nicht als Ordner angezeigt werden, können nur Programm gesteuert aufgerufen werden. Sammlungen dienen als Container für Elemente. Die Elemente in einer bestimmten Auflistung sind von einem konsistenten Typ. Das heißt, dass alle die gleiche Art von Element darstellen und eine beliebige Anzahl von Elementen in einer Auflistung vorhanden sein kann. Beispielsweise enthält die [**Anwendungs**](applications.md) Auflistung ein Element für jede com+-Anwendung, die auf dem Computer installiert ist. Diese Sammlung wird im Verwaltungs Tool als **com+-Anwendungs** Ordner angezeigt.

Die Auflistungen treten in einer hierarchischen Struktur auf, da die darin enthaltenen Elemente einer angeborenen Reihenfolge der Einfügung folgen. Da z. b. Komponenten in einer COM+-Anwendung installiert werden, wird die [**Komponenten**](components.md) Auflistung logisch unter der [**Anwendungs**](applications.md) Sammlung unterteilt. Vor allem, um die Komponenten zu speichern, die in dieser speziellen Anwendung installiert sind, gibt es für jedes Element in der **Anwendungs** Auflistung eine eindeutige **Komponenten** Sammlung.

Sie müssen immer dann eine Auflistung im Katalog abrufen, wenn Sie ein Element abrufen und Eigenschaften für dieses Element festlegen möchten. Im Allgemeinen müssen Sie mehrere Sammlungen schrittweise durchlaufen, um das gewünschte Element zu erhalten. Die Vorgehensweise hierzu finden Sie unter [Navigieren in der com+](navigating-the-com--collection-hierarchy.md)-Auflistungs Hierarchie.

Nachdem Sie eine Sammlung abgerufen haben und bevor Sie direkt mit den darin enthaltenen Elementen arbeiten können, müssen Sie die Sammlung auffüllen, die Daten für den Inhalt der Sammlung aus dem com+-Katalog abruft. Weitere Informationen finden Sie unter Auffüllen von [com+](populating-com--collections.md)-Auflistungen.

Außerdem gibt es eine Möglichkeit, die Sie verwenden können, mit der Sie dynamisch Abfragen können, um festzustellen, welche verwandten Sammlungen von einer bestimmten Sammlung verfügbar sind, die Sie halten. Weitere Informationen finden Sie unter [Abfragen von verfügbaren verwandten Sammlungen](querying-for-available-related-collections.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Verwaltungsvorgänge in Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



