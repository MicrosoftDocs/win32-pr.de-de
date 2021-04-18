---
description: Die meisten heute geschriebenen Anwendungen verarbeiten Zeichendaten in erster Linie als Unicode, wobei die UTF-16-Codierung verwendet wird.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Codepages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28528ba13e3db3f0c72dd7c071eb8b7886ab003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351713"
---
# <a name="code-pages"></a>Codepages

Die meisten heute geschriebenen Anwendungen verarbeiten Zeichendaten in erster Linie als [Unicode](unicode.md), wobei die UTF-16-Codierung verwendet wird. Viele Legacy Anwendungen verwenden jedoch weiterhin Zeichensätze auf der Grundlage von Codepages. Sogar neue Anwendungen müssen manchmal mit Codepages arbeiten, häufig aus einem der folgenden Gründe:

-   Für die Kommunikation mit Legacy Anwendungen.
-   Für die Kommunikation mit älteren Mail-und News-Servern, von denen möglicherweise nicht immer Unicode unterstützt wird.
-   Für die Kommunikation mit der Windows-Konsole.

> [!Note]  
> Neue Windows-Anwendungen sollten [Unicode](unicode.md) verwenden, um die Inkonsistenzen von unterschiedlichen Codepages und eine einfache Lokalisierung zu vermeiden.

 

Jede Codepage wird durch einen Code Page Bezeichner dargestellt, z. b. 1252, und wird von den Funktionen der Unicode-und Zeichensatz-API behandelt. Eine Liste der unterstützten Code Page Bezeichner finden Sie unter [Code Page Identifier](code-page-identifiers.md). Der Verweis "Codepages" im Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) bietet vollständige Beschreibungen vieler Codepages.

Windows-Codepages, häufig als "ANSI-Codepages" bezeichnet, sind Codepages, für die nicht-ASCII-Werte (Werte größer als 127) internationale Zeichen darstellen. Diese Codepages werden nativ in Windows Me verwendet und sind auch unter Windows NT und höher verfügbar.

> [!Note]  
> Ursprünglich war die Windows-Codepage 1252, die häufig für Englisch und andere westeuropäische Sprachen verwendete Codepage, auf einem American National Standards Institute (ANSI)-Entwurf basiert. Dieser Entwurf wurde schließlich ISO 8859-1, aber die Windows-Codepage 1252 wurde implementiert, bevor der Standard endgültig wurde, und ist nicht exakt identisch mit ISO 8859-1.

 

Viele Windows-API-Funktionen verfügen über die Versionen "A" (ANSI) und "W" (Wide, Unicode). Die "A"-Version verarbeitet Text, der auf Windows-Codepages basiert, während die "W"-Version Unicode-Text verarbeitet. Weitere Informationen finden Sie unter [Windows-Datentypen für](windows-data-types-for-strings.md) Zeichen folgen und [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md).

Windows-Codepages werden manchmal auch als "aktive Codepages" oder "System aktive Codepages" bezeichnet. Ein Windows-Betriebssystem verfügt immer über eine derzeit aktive Windows-Codepage. Alle [ANSI-Versionen von API-Funktionen](conventions-for-function-prototypes.md) verwenden die derzeit aktive Codepage.

Original Gerätehersteller (OEM)-Codepages sind Codepages, für die nicht-ASCII-Werte Zeilen Zeichnungs-und Interpunktions Zeichen darstellen. Diese Codepages wurden ursprünglich für MS-DOS verwendet und werden weiterhin für Konsolen Anwendungen verwendet. Sie werden auch für die nicht erweiterten Dateinamen in den Dateisystemen FAT12, FAT16 und FAT32 verwendet, wie in [Zeichensätzen, die in Dateinamen verwendet werden](character-sets-used-in-file-names.md), beschrieben. Die übliche OEM-Codepage für Englisch ist die Codepage 437.

Sowohl für Windows-Codepages als auch für OEM-Codepages entsprechen die Codewerte 0x00 bis 0x7F dem 7-Bit-ASCII-Zeichensatz. Die Codewerte 0x00 bis 0x19 und 0x7F stellen immer standardisierte Steuerzeichen und 0x20 bis 0x7E dar, die standardisierte darstellbare Zeichen darstellen. Zeichen, die durch die restlichen Codes, 0x80 bis 0xFF, dargestellt werden, variieren je nach Zeichensatz. Jeder Zeichensatz enthält verschiedene Sonderzeichen, die in der Regel für eine Sprache oder eine Gruppe von Sprachen angepasst sind. Die Windows-Codepage 1252 und die OEM-Codepage 437 werden im Allgemeinen in der USA verwendet.

Zusätzlich zu Windows-und OEM-Codepages können Ihre Anwendungen nicht systemeigene Codepages verwenden. Beispiele hierfür sind EBCDIC-und Macintosh-Codepages.

Zwei Codierungen von Unicode (UTF-7 und UTF-8) werden als Codepages implementiert. Wie andere Codepages ist jede Seite durch einen numerischen Bezeichner bekannt und kann mit vielen der gleichen Unicode-und Zeichensatz-API-Funktionen behandelt werden.

Codepages können als [Einzel Byte-Zeichensatz](single-byte-character-sets.md) Seiten (SBCS) oder [Doppelbyte-Zeichensatz](double-byte-character-sets.md) Seiten (DBCS) verwendet werden. In SBCS-Seiten codiert jedes Byte direkt ein einzelnes Zeichen, sodass es möglich ist, genau 256 unterschiedliche Zeichen (einschließlich Steuerzeichen, Buchstaben, Ziffern, Satzzeichen, Symbolen und ähnliches) darzustellen. DBCS-Codepages werden für Sprachen wie Japanisch und Chinesisch verwendet. In einer solchen Codepage verfügen einige Zeichen über zwei Byte-Codierungen mit bestimmten Byte Werten (immer Werte größer als 127), die als "Lead Bytes" fungieren. Anstatt Zeichen allein zu codieren, können führende Bytes einem Zeichen nur in Verbindung mit einem "Trail Byte" zugeordnet werden.

Einige Legacy Protokolle erfordern die Verwendung von SBCS-und DBCS-Codepages. Jede SBCS/DBCS-Codepage unterstützt unterschiedliche Zeichen, aber keine Codepage unterstützt die vollständige Breite der Zeichen, die von Unicode bereitgestellt werden. Jede SBCS/DBCS-Codepage unterstützt eine andere Teilmenge, unterschiedlich codiert.

> [!Note]  
> Daten, die von einer SBCS-oder DBCS-Codepage in eine andere konvertiert werden, unterliegen Beschädigungen, da der gleiche Datenwert auf unterschiedlichen Codepages ein anderes Zeichen codieren kann. Daten, die aus Unicode in SBCS oder DBCS konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes in den einzelnen Unicode-Daten verwendete Zeichen darstellen kann.

 

Zusätzlich zu SBCS-und DBCS-Codepages stehen Ihren Anwendungen die Multibytezeichen-Zeichensatz-Codepages 52936, 54936, 51949 und 5022x zur Verfügung, die einen ähnlichen Ansatz wie bei einem DBCS verwenden. Eine Multibytezeichen-Zeichensatz-Codepage geht jedoch über zwei Byte-Codierungen einiger Zeichen hinaus. UTF-7 und UTF-8 verwenden einen ähnlichen Ansatz zum Codieren von Unicode basierend auf einem 7-Bit-bzw. 8-Bit-Bytes. Weitere Informationen finden Sie unter [Unicode](unicode.md).

Mehrere Unicode-und Zeichensatz Funktionen ermöglichen es Ihren Anwendungen, Codepages zu verarbeiten. Eine Anwendung kann die Funktionen " [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) " und " [**getcpinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) " verwenden, um Informationen über eine Codepage zu erhalten. Diese Informationen enthalten das Standard Zeichen, das verwendet wird, wenn ein Zeichen in einer konvertierten Zeichenfolge über keinen entsprechenden Eintrag in der Codepage verfügt.

Eine Anwendung kann die Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwenden, um Zeichen folgen auf der Grundlage von Windows-Codepages und Unicode-Zeichen folgen zu konvertieren. Obwohl ihre Namen auf "Multibytezeichen" verweisen, funktionieren diese Funktionen mit SBCS-, DBCS-und Multibytezeichen-Zeichensatz-Codepages gleichermaßen gut.

> [!Note]  
> Bei [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) können einige Daten verloren gehen, wenn die angegebene Codepage nicht alle Zeichen in einer Unicode-Zeichenfolge darstellen kann.

 

Die Anwendung kann mithilfe der Standardfunktionen der C-Lauf Zeit Bibliothek zwischen Windows-Codepages und OEM-Codepages konvertieren. Die Verwendung dieser Funktionen stellt jedoch das Risiko von Datenverlusten dar, da die Zeichen, die von jeder Codepage dargestellt werden können, nicht genau übereinstimmen.

Ihre Anwendungen können auch die [**GetACP-**](/windows/desktop/api/Winnls/nf-winnls-getacp) Funktion aufrufen. Diese Funktion Ruft den Bezeichner der aktuellen Windows (ANSI)-Codepage ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> </dl>

 

 



