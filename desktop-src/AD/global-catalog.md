---
title: Globaler Katalog
description: Eine Domäne, die von Active Directory Domain Services ausgeführt wird, kann aus vielen Partitionen oder namens Kontexten bestehen.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- globaler Katalog Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4496804d21e53cf2d87947288179e7f96ca75c8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724512"
---
# <a name="global-catalog"></a>Globaler Katalog

Eine Domäne, die von Active Directory Domain Services ausgeführt wird, kann aus vielen Partitionen oder namens Kontexten bestehen. Der Distinguished Name (DN) eines Objekts enthält ausreichend Informationen, um nach einem Replikat der Partition zu suchen, die das Objekt enthält. Häufig ist es jedoch nicht möglich, dass der Benutzer oder die Anwendung den DN des Zielobjekts oder die Partition, in der das Objekt enthalten ist, kennt. Der [*globale Katalog (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) ermöglicht Benutzern und Anwendungen das Auffinden von Objekten in einer Active Directory Domänen Struktur mit einem oder mehreren Attributen des Zielobjekts.

Der globale Katalog enthält ein partielles Replikat jedes namens Kontexts im Verzeichnis. Sie enthält auch die Schema-und Konfigurations Namenskontexte. Dies bedeutet, dass der GC ein Replikat jedes Objekts im Verzeichnis enthält, aber nur eine kleine Anzahl von Attributen enthält. Die Attribute in der GC sind diejenigen, die am häufigsten in Such Vorgängen verwendet werden (z. b. die vor-und Nachnamen eines Benutzers oder Anmelde Namen), und diejenigen, die zum Suchen eines vollständigen Replikats des Objekts erforderlich sind. Die GC ermöglicht es Benutzern, interessante Objekte schnell zu finden, ohne zu wissen, welche Domäne Sie enthält und ohne dass ein zusammenhängender erweiterter Namespace im Unternehmen erforderlich ist.

Der globale Katalog wird automatisch vom Active Directory Domain Services Replikationssystem erstellt. Die Replikations Topologie für den globalen Katalog wird automatisch generiert. Die Eigenschaften, die in den globalen Katalog repliziert werden, enthalten ein von Microsoft definiertes Basisset. Administratoren können zusätzliche Eigenschaften angeben, um die Anforderungen Ihrer Installation zu erfüllen.

 

 