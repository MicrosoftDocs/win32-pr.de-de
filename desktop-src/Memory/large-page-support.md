---
description: Die Unterstützung für große Seiten ermöglicht es Server Anwendungen, große Speicherbereiche zu erstellen, was besonders für 64-Bit-Windows nützlich ist.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Large-Page Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4578b5127e6613f2ff4b6e0b8a7cffcc53c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348191"
---
# <a name="large-page-support"></a>Large-Page Unterstützung

Die Unterstützung für große Seiten ermöglicht es Server Anwendungen, große Speicherbereiche zu erstellen, was besonders für 64-Bit-Windows nützlich ist. Jede Übersetzung der großen Seite verwendet einen einzelnen Übersetzungs Puffer innerhalb der CPU. Die Größe dieses Puffers beträgt in der Regel drei Größenordnungen, die größer als die systemeigene Seitengröße sind. Dies erhöht die Effizienz des Übersetzungs Puffers, wodurch die Leistung für häufig verwendeten Arbeitsspeicher gesteigert werden kann.

Im folgenden Verfahren wird beschrieben, wie die Unterstützung für große Seiten verwendet wird.

**So verwenden Sie die Unterstützung für große Seiten**

1.  Rufen Sie die **SeLockMemoryPrivilege** -Berechtigung durch Aufrufen der Funktion " [**switchtokenprivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " ab. Weitere Informationen finden Sie unter [Zuweisen von Berechtigungen zu einem Konto](../secbp/assigning-privileges-to-an-account.md) und [Ändern von Berechtigungen in einem Token](../secbp/changing-privileges-in-a-token.md).
2.  Rufen Sie die minimale Größe der großen Seite ab, indem Sie die [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) -Funktion aufrufen.
3.  Fügen Sie beim Aufrufen der [**virtualdepc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion den Wert für hohe SKU- **\_ \_ Seiten** ein. Die Größe und die Ausrichtung müssen ein Vielfaches des minimalen großen Seiten Werte sein.

Beachten Sie beim Schreiben von Anwendungen, die großen Seiten Speicher verwenden, die folgenden Überlegungen:

-   Das Abrufen von Speicherbereichen für große Seiten ist möglicherweise schwierig, nachdem das System lange ausgeführt wurde, da der physische Speicherplatz für jede große Seite zusammenhängend sein muss, der Arbeitsspeicher jedoch möglicherweise fragmentiert wurde. Das Zuordnen von großen Seiten unter diesen Bedingungen kann die Systemleistung erheblich beeinträchtigen. Daher sollten Anwendungen keine wiederholten Zuordnungen für große Seiten erstellen und stattdessen alle großen Seiten beim Start einmal zuordnen.
-   Der Arbeitsspeicher ist immer Lese-/Schreibzugriff und nicht auslagerbar (immer im physischen Speicher ansässig).
-   Der Arbeitsspeicher ist Teil der privaten Bytes für den Prozess, aber nicht Teil des Workingsets, da der Workingset definitionsgemäß nur den Speicherplatz enthält.
-   Die Zuordnung von großen Seiten unterliegt nicht den Auftrags Grenzen.
-   Der Speicher für große Seiten muss reserviert und als einzelner Vorgang ausgeführt werden. Mit anderen Worten: große Seiten können nicht verwendet werden, um einen Commit für einen zuvor reservierten Speicherbereich durchzusetzen.
-   WOW64 auf Intel Itanium-basierten Systemen unterstützt keine 32-Bit-Anwendungen, die dieses Feature verwenden. Die Anwendungen sollten als native 64-Bit-Anwendungen neu kompiliert werden.

 

 
