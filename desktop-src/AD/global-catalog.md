---
title: Globaler Katalog
description: Eine Domäne, die von Active Directory Domain Services ausgeführt wird, kann aus vielen Partitionen oder Namenskontexten bestehen.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- Globaler Active Directory-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81abf04ab3e4d95819f91b5db8753a265e49ca79b2f405a32665dc46a8f2db5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189115"
---
# <a name="global-catalog"></a>Globaler Katalog

Eine Domäne, die von Active Directory Domain Services ausgeführt wird, kann aus vielen Partitionen oder Namenskontexten bestehen. Der Distinguished Name (DN) eines Objekts enthält genügend Informationen, um ein Replikat der Partition zu finden, die das Objekt enthält. Häufig kennt der Benutzer oder die Anwendung jedoch nicht den DN des Zielobjekts oder die Partition, die das Objekt enthalten kann. Mit dem [*globalen Katalog (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) können Benutzer und Anwendungen Objekte in einer Active Directory-Domänenstruktur suchen, wenn mindestens ein Attribut des Zielobjekts vorhanden ist.

Der globale Katalog enthält ein Teilreplikat jedes Namenskontexts im Verzeichnis. Sie enthält auch die Schema- und Konfigurationsbenennungskontexte. Dies bedeutet, dass die GC ein Replikat jedes Objekts im Verzeichnis enthält, jedoch nur mit einer kleinen Anzahl ihrer Attribute. Die Attribute in der GC sind die attribute, die am häufigsten in Suchvorgängen verwendet werden (z. B. Vor- und Nachnamen oder Anmeldenamen eines Benutzers) und die attribute, die zum Suchen eines vollständigen Replikats des Objekts erforderlich sind. Mit der GC können Benutzer objekte von Interesse schnell finden, ohne zu wissen, welche Domäne sie enthält, und ohne dass ein zusammenhängender erweiterter Namespace im Unternehmen erforderlich ist.

Der globale Katalog wird automatisch vom Active Directory Domain Services Replikationssystem erstellt. Die Replikationstopologie für den globalen Katalog wird automatisch generiert. Die im globalen Katalog replizierten Eigenschaften enthalten einen von Microsoft definierten Basissatz. Administratoren können zusätzliche Eigenschaften angeben, um die Anforderungen ihrer Installation zu erfüllen.

 

 