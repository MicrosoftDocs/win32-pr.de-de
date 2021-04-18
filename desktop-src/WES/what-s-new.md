---
title: Neuigkeiten (Windows-Ereignisprotokoll)
description: Auf dieser Seite werden die neuen Features zusammengefasst, die der Windows-Ereignisprotokoll-API für die einzelnen Releases hinzugefügt wurden.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652d82f67292316dd7aec599955d69dd70ab39a3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340555"
---
# <a name="whats-new-windows-event-log"></a>Neuigkeiten (Windows-Ereignisprotokoll)

Auf dieser Seite werden die neuen Features zusammengefasst, die der Windows-Ereignisprotokoll-API für die einzelnen Releases hinzugefügt wurden.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Im folgenden finden Sie die Änderungen, die am [Event Manifest](eventmanifestschema-schema.md) -Schema vorgenommen wurden:

-   Der komplexe Typ " [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) " wurde entfernt. Um die gleiche Funktionalität bereitzustellen, verwenden Sie aufgabenspezifische Opcodes (Weitere Informationen finden Sie im **Opcodes** -Element des komplexen [**TaskType**](eventmanifestschema-tasktype-complextype.md) -Typs.
-   Die einfachen Typen " [**csymboltype**](eventmanifestschema-csymboltype-simpletype.md)", " [**FilePath**](eventmanifestschema-filepath-simpletype.md)" und " [**strautableref**](eventmanifestschema-strtableref-simpletype.md) " wurden hinzugefügt, um die den Attributen dieser Typen zugewiesenen Werte einzuschränken.
-   Das **Filters** -Attribut wurde dem komplexen [**ProviderType**](eventmanifestschema-providertype-complextype.md) -Typ hinzugefügt. Anbieter können Filter auf die gleiche Weise verwenden, wie-Anbieter Ebenen und Schlüsselwörter verwenden, um zu bestimmen, ob Sie ein Ereignis schreiben sollten.
-   Die folgenden Ausgabetypen wurden hinzugefügt, die Sie für Datenelemente angeben können, die in einer Ereignisdaten Vorlage definiert sind:
    -   Win: datetimecultureinsensitive
    -   Win: HRESULT
    -   Win: NTSTATUS
-   Die Ausgabetypen werden nun berücksichtigt, wohingegen Sie ignoriert wurden.

Die folgenden Änderungen wurden an der Version des [**Nachrichten Compilers**](message-compiler--mc-exe-.md) vorgenommen, der mit der Windows 7-Version der Windows SDK ausgeliefert wird:

-   Es wurden Argumente hinzugefügt, damit der Compiler Protokollierungs Code basierend auf dem Manifest generiert. Sie können auch anfordern, dass der Compiler Code generiert, um Ereignisse auf Betriebssystemen vor Windows Vista zu protokollieren. Eine Liste der Argumente finden Sie im Abschnitt "Argumente, die für das Erstellen von Code zum Protokollieren von Ereignissen verwendet werden" im Thema " [**Nachrichten Compiler**](message-compiler--mc-exe-.md) ".
-   Der Compiler erzwingt nun eine strengere syntaktische und semantische Validierung für das Manifest. Dies kann dazu führen, dass einige Manifeste, die erfolgreich in früheren Versionen des Nachrichten Compilers kompiliert wurden, Änderungen erfordern, damit Sie erfolgreich mit der aktuellen Version kompiliert werden können.
