---
description: 'Windows API-Funktionen, die Zeichen bearbeiten, werden in der Regel in einem von drei Formaten implementiert:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode in der Windows-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c36e1e292eddd786d4c4bf336f980486f66870deb809587f9c51334f269ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764810"
---
# <a name="unicode-in-the-windows-api"></a>Unicode in der Windows-API

Windows API-Funktionen, die Zeichen bearbeiten, werden in der Regel in einem von drei Formaten implementiert:

-   Eine generische Version, die entweder für Windows Codepages oder Unicode kompiliert werden kann.
-   Eine [Windows Codepageversion](code-pages.md) mit dem Buchstaben "A", mit dem "ANSI" angegeben wird
-   Eine [Unicode-Version](unicode.md) mit dem Buchstaben "W", mit dem "wide" angegeben wird

Einige neuere Funktionen unterstützen nur Unicode-Versionen. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen.](conventions-for-function-prototypes.md)

In den folgenden Themen werden Unicode-Datentypen und deren Verwendung in Funktionen und Nachrichten erläutert. die Verwendung von Ressourcen, Dateinamen und Befehlszeilenargumenten; - und -Methoden zum Übersetzen zwischen verschiedenen Zeichenfolgentypen.

-   [Automatische Nachrichtenübersetzung](automatic-message-translation.md)
-   [In Dateinamen verwendete Zeichensätze](character-sets-used-in-file-names.md)
-   [Befehlszeilenargumente](command-line-arguments.md)
-   [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)
-   [C-Standardfunktionen](standard-c-functions.md)
-   [Unterschiede zwischen Zeichenfolgenfunktionen](string-function-differences.md)
-   [Übersetzung zwischen Zeichenfolgentypen](translation-between-string-types.md)
-   [Windows-Datentypen für Zeichenfolgen](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Unicode und Zeichensätzen](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



