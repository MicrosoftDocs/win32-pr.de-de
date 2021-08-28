---
title: What es New (Windows Event Log)
description: Auf dieser Seite werden die neuen Features zusammengefasst, die der Windows-Ereignisprotokoll-API für jedes Release hinzugefügt wurden.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f80af15d6f8b6d95533fff296ee22ea3c82d2add5f21964a7863ac3d676f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904120"
---
# <a name="whats-new-windows-event-log"></a>What es New (Windows Event Log)

Auf dieser Seite werden die neuen Features zusammengefasst, die der Windows-Ereignisprotokoll-API für jedes Release hinzugefügt wurden.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Im Folgenden finden Sie die Änderungen, die am [EventManifest-Schema vorgenommen](eventmanifestschema-schema.md) wurden:

-   Der komplexe [**Typ TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) wurde entfernt. Um die gleiche Funktionalität zu bieten, verwenden Sie aufgabenspezifische Opcodes (siehe **das opcodes-Element** des komplexen [**TaskType-Typs).**](eventmanifestschema-tasktype-complextype.md)
-   Die [**einfachen Typen CSymbolType,**](eventmanifestschema-csymboltype-simpletype.md) [**filePath**](eventmanifestschema-filepath-simpletype.md)und [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) wurden hinzugefügt, um Werte einzuschränken, die Attributen dieser Typen zugewiesen sind.
-   Das **Filterattribut** wurde dem komplexen [**ProviderType-Typ**](eventmanifestschema-providertype-complextype.md) hinzugefügt. Anbieter können Filter auf die gleiche Weise wie Anbieter verwenden, um zu bestimmen, ob sie ein Ereignis schreiben sollen.
-   Die folgenden Ausgabetypen wurden hinzugefügt, die Sie für Datenelemente angeben können, die in einer Ereignisdatenvorlage definiert sind:
    -   win:DateTimeCultureInsensitive
    -   win:HResult
    -   win:NTSTATUS
-   Die Ausgabetypen werden jetzt berücksichtigt, während sie vor ignoriert wurden.

Die folgenden Änderungen wurden an [](message-compiler--mc-exe-.md) der Version des Nachrichtencompilers vorgenommen, die im Windows 7-Version des Windows SDK enthalten ist:

-   Argumente wurden hinzugefügt, damit der Compiler Protokollierungscode basierend auf Ihrem Manifest generiert. Sie können auch anfordern, dass der Compiler Code generiert, um Ereignisse auf Betriebssystemen zu protokollieren, bevor Windows Vista ausgeführt wird. Eine Liste der Argumente finden Sie im Abschnitt "Argumente für das Generieren von Code, der zum Protokollieren von Ereignissen verwendet wird" des Themas [**Nachrichtencompiler.**](message-compiler--mc-exe-.md)
-   Der Compiler erzwingt jetzt eine strengere syntaktische und semantische Validierung für das Manifest. Dies kann dazu führen, dass einige Manifeste, die erfolgreich in früheren Versionen des Nachrichtencompilers kompiliert wurden, Änderungen erfordern, um erfolgreich mit der neuesten Version kompiliert zu werden.
