---
description: 'Windows-API-Funktionen, die Zeichen bearbeiten, werden im Allgemeinen in einem von drei Formaten implementiert:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode in der Windows-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373161"
---
# <a name="unicode-in-the-windows-api"></a>Unicode in der Windows-API

Windows-API-Funktionen, die Zeichen bearbeiten, werden im Allgemeinen in einem von drei Formaten implementiert:

-   Eine generische Version, die für Windows-Codepages oder Unicode kompiliert werden kann.
-   Eine [Windows-Codepage](code-pages.md) -Version mit dem Buchstaben "A", mit der "ANSI" angegeben wird.
-   Eine [Unicode](unicode.md) -Version mit dem Buchstaben "W", die "Wide" angibt

Einige neuere Funktionen unterstützen nur Unicode-Versionen. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md).

In den folgenden Themen finden Sie Informationen zu Unicode-Datentypen und deren Verwendung in Funktionen und Nachrichten. Verwendung von Ressourcen, Dateinamen und Befehlszeilen Argumenten und Methoden zum Übersetzen zwischen verschiedenen Zeichen folgen Typen.

-   [Automatische Nachrichten Übersetzung](automatic-message-translation.md)
-   [In Dateinamen verwendete Zeichensätze](character-sets-used-in-file-names.md)
-   [Befehlszeilenargumente](command-line-arguments.md)
-   [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)
-   [Standard-C-Funktionen](standard-c-functions.md)
-   [Unterschiede in Zeichen folgen](string-function-differences.md)
-   [Übersetzung zwischen Zeichen folgen Typen](translation-between-string-types.md)
-   [Windows-Datentypen für Zeichenfolgen](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Unicode und Zeichensätzen](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



