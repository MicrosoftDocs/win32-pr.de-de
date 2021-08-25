---
description: Die Unterstützung für große Seiten ermöglicht Es Serveranwendungen, Speicherbereiche für große Seiten einzurichten. Dies ist besonders bei 64-Bit-Windows nützlich.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Large-Page-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad61873c80d2d3fe8de6a915f5eb93f527049a437860deabedbe232cdf9cb885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869680"
---
# <a name="large-page-support"></a>Large-Page-Unterstützung

Die Unterstützung für große Seiten ermöglicht Es Serveranwendungen, Speicherbereiche für große Seiten einzurichten. Dies ist besonders bei 64-Bit-Windows nützlich. Jede Großseitenübersetzung verwendet einen einzelnen Übersetzungspuffer innerhalb der CPU. Die Größe dieses Puffers ist in der Regel um drei Größenordnungen größer als die größe der nativen Seite. Dies erhöht die Effizienz des Übersetzungspuffers, wodurch die Leistung für häufig genutzten Arbeitsspeicher erhöht werden kann.

Im folgenden Verfahren wird die Verwendung der Unterstützung für große Seiten beschrieben.

**So verwenden Sie die Unterstützung für große Seiten**

1.  Rufen Sie die **SeLockMemoryPrivilege-Berechtigung** ab, indem Sie die [**Funktion AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) aufrufen. Weitere Informationen finden Sie unter [Zuweisen von Berechtigungen zu einem Konto](../secbp/assigning-privileges-to-an-account.md) und Ändern von Berechtigungen in einem [Token.](../secbp/changing-privileges-in-a-token.md)
2.  Rufen Sie die minimale Größe für große Seiten ab, indem Sie die [**GetLargePageMinimum-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) aufrufen.
3.  Schließen Sie den **MEM \_ LARGE \_ PAGES-Wert** ein, wenn Sie die [**VirtualAlloc-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) aufrufen. Größe und Ausrichtung müssen ein Vielfaches des Minimums für große Seiten sein.

Beachten Sie beim Schreiben von Anwendungen, die großen Seitenspeicher verwenden, die folgenden Aspekte:

-   Speicherbereiche für große Seiten können schwierig zu erhalten sein, nachdem das System für eine lange Zeit ausgeführt wurde, da der physische Platz für jede große Seite zusammenhängend sein muss, aber der Arbeitsspeicher möglicherweise fragmentiert wurde. Das Zuordnen großer Seiten unter diesen Bedingungen kann sich erheblich auf die Systemleistung auswirken. Daher sollten Anwendungen vermeiden, wiederholte Zuordnungen für große Seiten vorzunehmen und stattdessen alle großen Seiten beim Start einmal zuzuordnen.
-   Der Arbeitsspeicher ist immer lese-/schreibbar und nicht auslagerungsfähig (immer im physischen Speicher vorhanden).
-   Der Arbeitsspeicher ist Teil des Prozesses privater Bytes, aber nicht Teil des Arbeitssatzes, da der Arbeitssatz definitionsgemäß nur auslagerungsfähigen Arbeitsspeicher enthält.
-   Für Umfangreiche Seitenzuordnungen gelten keine Auftragsgrenzwerte.
-   Der Arbeitsspeicher für große Seiten muss reserviert und als einzelner Vorgang ausgeführt werden. Mit anderen Worten: Große Seiten können nicht zum Committen eines zuvor reservierten Speicherbereichs verwendet werden.
-   WOW64 auf Intel Itanium-basierten Systemen unterstützt keine 32-Bit-Anwendungen, die dieses Feature verwenden. Die Anwendungen sollten als native 64-Bit-Anwendungen neu kompiliert werden.

 

 
