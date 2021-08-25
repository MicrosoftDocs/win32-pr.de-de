---
description: Bereitstellen für schnellere Kommunikation
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Bereitstellen für schnellere Kommunikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201185878a6d3fc041512b41fd3f51975ae5e0988f853dbbbcb77b716ea4cebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070780"
---
# <a name="deploying-for-faster-communication"></a>Bereitstellen für schnellere Kommunikation

Die Leistung ist ein wichtiger Aspekt bei der Bereitstellung einer COM+-Anwendung, und der Speicherort der Komponente ist der Schlüssel, um die beste Leistung aus einer gut entworfenen Anwendung zu erzielen.

Früher wurde allgemein festgestellt, dass mit skalierbaren Anwendungsarchitekturen die Leistung durch einfaches Verschieben primärer Komponenten der Anwendung auf schnellere Hardware behoben werden kann. Dies hat sich als nicht wahr erwiesen. Leistungsprobleme entstehen nicht durch die Leistung einzelner Komponenten, sondern durch die Links, die Komponenten verbinden.

Der primäre Faktor für den Erfolg ist der Standort. Nähe oder physischer Standort, Zeit, Kapazität und Zweck sind unterschiedliche Aspekte des Standorts, die für die Bereitstellung einer COM+-Anwendung gelten und sich alle auf die Leistung auswirken.

Die beste Leistung erzielen Sie, wenn die Anwendungskomponenten und -ressourcen so entworfen und bereitgestellt werden, dass sie den Anforderungen der Anwendungsworkload entsprechen.

Im Allgemeinen sollten Sie Komponenten bereitstellen, um die prozess- und insbesondere computerübergreifende Kommunikation zwischen Komponenten zu minimieren. Wenn Ihr Anwendungsentwurf effizient ist, werden Klassen innerhalb einer Komponente nach Verwendung und Funktion gruppiert, um die Kommunikation innerhalb von Komponenten zu maximieren. Beim Bereitstellen von Komponenten müssen Sie sicherstellen, dass die Komponenten logisch angeordnet sind, um die Beziehungen zwischen den Komponenten zu nutzen und die Menge an Messaging zwischen Komponenten zu reduzieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen für die Bereitstellung](designing-for-deployment.md)
</dt> </dl>

 

 



