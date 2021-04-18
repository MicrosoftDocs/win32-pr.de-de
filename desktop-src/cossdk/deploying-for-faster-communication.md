---
description: Bereitstellen für schnellere Kommunikation
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Bereitstellen für schnellere Kommunikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345636"
---
# <a name="deploying-for-faster-communication"></a>Bereitstellen für schnellere Kommunikation

Die Leistung ist ein wichtiger Aspekt bei der Bereitstellung einer COM+-Anwendung, und der Speicherort der Komponente ist der Schlüssel zum erzielen der besten Leistung einer gut entworfenen Anwendung.

Es war in der Zwischenzeit mit skalierbaren Anwendungsarchitekturen, dass die Leistung durch einfaches Verschieben der primären Komponenten der Anwendung auf schnellere Hardware gelöst werden konnte. Dies hat sich als nicht wahr erwiesen. Leistungsprobleme treten nicht aus der Leistung einzelner Komponenten, sondern von den Verknüpfungen, die Komponenten verbinden, auf.

Der primäre Faktor für den Erfolg ist die Position. Near oder physischer Standort, Zeit, Kapazität und Zweck sind unterschiedliche Aspekte des Standorts, die für die Bereitstellung einer COM+-Anwendung gelten, die sich alle auf die Leistung auswirken.

Die beste Leistung ist, wenn die Anwendungskomponenten und-Ressourcen entworfen und bereitgestellt werden, um die Anforderungen zu erfüllen, die von der Arbeitsauslastung der Anwendung auf diese angewendet werden

Im Allgemeinen sollten Sie Komponenten bereitstellen, um prozessübergreifende und besonders Computer übergreifende Kommunikation zwischen Komponenten zu minimieren. Wenn ihr Anwendungs Entwurf effizient ist, werden Klassen innerhalb einer Komponente nach Verwendung und Funktion gruppiert, um die Kommunikation innerhalb von Komponenten zu maximieren. Beim Bereitstellen von Komponenten müssen Sie sicherstellen, dass sich die Komponenten logisch befinden, um die Beziehungen zwischen den Komponenten zu nutzen und die Menge an Messaging zwischen den Komponenten zu verringern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen für die Bereitstellung](designing-for-deployment.md)
</dt> </dl>

 

 



