---
description: Die meisten heute geschriebenen Anwendungen verarbeiten Zeichendaten in erster Linie als Unicode unter Verwendung der UTF-16-Codierung.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Codepages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad589183bbb64a2feb65079a2322dd148598c6c3542320ec2ce851b9de61cfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754960"
---
# <a name="code-pages"></a>Codepages

Die meisten heute geschriebenen Anwendungen verarbeiten Zeichendaten in erster Linie als [Unicode](unicode.md)mithilfe der UTF-16-Codierung. Viele Ältere Anwendungen verwenden jedoch weiterhin Zeichensätze, die auf Codepages basieren. Auch neue Anwendungen müssen manchmal mit Codepages arbeiten, häufig aus einem der folgenden Gründe:

-   Für die Kommunikation mit Legacyanwendungen.
-   Für die Kommunikation mit älteren E-Mail- und News-Servern, die Unicode möglicherweise nicht immer unterstützen.
-   Für die Kommunikation mit der Windows Console.

> [!Note]  
> Neue Windows sollten [Unicode](unicode.md) verwenden, um inkonsistente Codepages zu vermeiden und die Lokalisierung zu erleichtern.

 

Jede Codepage wird durch einen Codepagebezeichner dargestellt, z. B. 1252, und wird von den Unicode- und Zeichensatz-API-Funktionen verarbeitet. Eine Liste der unterstützten Codepagebezeichner finden Sie unter [Codepagebezeichner](code-page-identifiers.md). Die Referenz zu "Codepages" im Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) enthält vollständige Beschreibungen vieler Codepages.

Windows Codepages, die häufig als "ANSI-Codepages" bezeichnet werden, sind Codepages, für die Nicht-ASCII-Werte (Werte größer als 127) internationale Zeichen darstellen. Diese Codepages werden nativ in Windows Me verwendet und sind auch auf Windows NT und höher verfügbar.

> [!Note]  
> Ursprünglich basiert Windows Codepage 1252 häufig für Englisch und andere weste europäische Sprachen verwendete Codepage auf einem entwurf American National Standards Institute (ANSI). Dieser Entwurf wurde schließlich zu ISO 8859-1, aber Windows Codepage 1252 wurde implementiert, bevor der Standard endgültig wurde, und ist nicht genau identisch mit ISO 8859-1.

 

Viele Windows-API-Funktionen verfügen über die Versionen "A" (ANSI) und "W" (breit, Unicode). Die Version "A" verarbeitet Text basierend auf Windows Codepages, während die W-Version Unicode-Text verarbeitet. Siehe [Windows Datentypen für Zeichenfolgen und](windows-data-types-for-strings.md) [Konventionen für Funktionsprototypen.](conventions-for-function-prototypes.md)

Windows Codepages werden manchmal auch als "aktive Codepages" oder "systemaktive Codepages" bezeichnet. Ein Windows betriebssystem verfügt immer über eine derzeit aktive Windows Codepage. Alle [ANSI-Versionen von API-Funktionen](conventions-for-function-prototypes.md) verwenden die derzeit aktive Codepage.

OEM-Codepages (Original Equipment Manufacturer) sind Codepages, für die Nicht-ASCII-Werte Zeichen für Linienzeichnung und Interpunktion darstellen. Diese Codepages wurden ursprünglich für MS-DOS verwendet und werden weiterhin für Konsolenanwendungen verwendet. Sie werden auch für die nicht erweiterten Dateinamen in den Dateisystemen FAT12, FAT16 und FAT32 verwendet, wie unter In Dateinamen verwendete Zeichensätze [beschrieben.](character-sets-used-in-file-names.md) Die übliche OEM-Codepage für Englisch ist Codepage 437.

Sowohl für Windows Codepages als auch für OEM-Codepages entsprechen die Codewerte 0x00 bis 0x7F dem 7-Bit-ASCII-Zeichensatz. Codewerte, 0x00 durch 0x19 und 0x7F werden, stellen immer standardisierte Steuerzeichen dar, und 0x20 bis 0x7E standardisierte anzeigebare Zeichen darstellen. Zeichen, die durch die verbleibenden Codes dargestellt 0x80 bis 0xff, variieren je nach Zeichensatz. Jeder Zeichensatz enthält verschiedene Sonderzeichen, die in der Regel für eine Sprache oder Eine Gruppe von Sprachen angepasst werden. Windows Codepage 1252 und OEM-Codepage 437 werden in der Regel in der USA.

Zusätzlich zu Windows und OEM-Codepages können Ihre Anwendungen nicht native Codepages verwenden. Beispiele hierfür sind EBCDIC- und Macintosh-Codepages.

Zwei Unicode-Codierungen (UTF-7 und UTF-8) werden als Codepages implementiert. Wie andere Codepages ist jede Seite durch einen numerischen Bezeichner bekannt und kann mit vielen der gleichen Unicode- und Zeichensatz-API-Funktionen verarbeitet werden.

Codepages können entweder [SBCS-Seiten (Single-Byte Character Set)](single-byte-character-sets.md) oder DBCS-Seiten [(Double-Byte Character Set)](double-byte-character-sets.md) sein. Auf SBCS-Seiten codiert jedes Byte direkt ein einzelnes Zeichen, sodass genau 256 unterschiedliche Zeichen dargestellt werden können (einschließlich Steuerzeichen, Buchstaben, Ziffern, Interpunktion, Symbole und Deren). DBCS-Codepages werden für Sprachen wie Japanisch und Chinesisch verwendet. In einer solchen Codepage verfügen einige Zeichen über 2-Byte-Codierungen mit bestimmten Bytewerten (immer Werte größer als 127), die als "Leadbytes" dienen. Anstatt Zeichen selbst zu codieren, können Leadbytes nur in Verbindung mit einem "trail byte" einem Zeichen zugeordnet werden.

Einige Ältere Protokolle erfordern die Verwendung von SBCS- und DBCS-Codepages. Jede SBCS/DBCS-Codepage unterstützt unterschiedliche Zeichen, aber keine Codepage unterstützt die gesamte Breite der von Unicode bereitgestellten Zeichen. Jede SBCS/DBCS-Codepage unterstützt eine andere Teilmenge, die unterschiedlich codiert ist.

> [!Note]  
> Daten, die von einer SBCS- oder DBCS-Codepage in eine andere konvertiert werden, unterliegen einer Beschädigung, da derselbe Datenwert auf verschiedenen Codepages ein anderes Zeichen codieren kann. Daten, die von Unicode in SBCS oder DBCS konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes zeichen darstellen kann, das in diesen bestimmten Unicode-Daten verwendet wird.

 

Zusätzlich zu SBCS- und DBCS-Codepages verfügen Ihre Anwendungen über die Multibyte-Zeichensatz-Codepages 52936, 54936, 51949 und 5022x, die einen ähnlichen Ansatz wie bei einem DBCS verwenden. Eine Multibyte-Zeichensatz-Codepage geht jedoch über die Zwei-Byte-Codierung einiger Zeichen hinaus. UTF-7 und UTF-8 verwenden einen ähnlichen Ansatz zum Codieren von Unicode basierend auf 7-Bit- bzw. 8-Bit-Bytes. Weitere Informationen finden Sie unter [Unicode](unicode.md).

Mehrere Unicode- und Zeichensatzfunktionen ermöglichen Es Ihren Anwendungen, Codepages zu verarbeiten. Eine Anwendung kann die [**Funktionen GetCPInfo und**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) verwenden, um Informationen zu einer Codepage zu erhalten. Diese Informationen umfassen das Standardzeichen, das verwendet wird, wenn ein Zeichen in einer konvertierten Zeichenfolge keinen entsprechenden Eintrag in der Codepage aufgibt.

Eine Anwendung kann die [**Funktionen MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwenden, um zwischen Zeichenfolgen zu konvertieren, die auf Windows Codepages und Unicode-Zeichenfolgen basieren. Obwohl ihre Namen auf "MultiByte" verweisen, funktionieren diese Funktionen genauso gut mit SBCS-, DBCS- und Multibyte-Zeichensatz-Codepages.

> [!Note]  
> [**WideCharToMultiByte kann einige**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) Daten verlieren, wenn die angegebene Codepage nicht alle Zeichen in einer Unicode-Zeichenfolge darstellen kann.

 

Ihre Anwendung kann mithilfe der standardmäßigen C-Laufzeitbibliotheksfunktionen zwischen Windows Codepages und OEM-Codepages konvertieren. Die Verwendung dieser Funktionen birgt jedoch das Risiko eines Datenverlusts, da die Zeichen, die von jeder Codepage dargestellt werden können, nicht genau übereinstimmen.

Ihre Anwendungen können auch die [**GetACP-Funktion**](/windows/desktop/api/Winnls/nf-winnls-getacp) aufrufen. Diese Funktion ruft den Bezeichner der aktuellen Windows Codepage (ANSI) ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> </dl>

 

 



