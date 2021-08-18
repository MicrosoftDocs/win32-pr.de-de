---
description: Die meisten heute geschriebenen Anwendungen verarbeiten Zeichendaten hauptsächlich als Unicode mithilfe der UTF-16-Codierung.
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

Die meisten heute geschriebenen Anwendungen verarbeiten Zeichendaten hauptsächlich als [Unicode](unicode.md)mithilfe der UTF-16-Codierung. Viele Legacyanwendungen verwenden jedoch weiterhin Zeichensätze, die auf Codepages basieren. Selbst neue Anwendungen müssen manchmal mit Codepages arbeiten, häufig aus einem der folgenden Gründe:

-   Für die Kommunikation mit Legacyanwendungen.
-   Für die Kommunikation mit älteren E-Mail- und News-Servern, die Unicode möglicherweise nicht immer unterstützen.
-   Um mit der Windows-Konsole zu kommunizieren.

> [!Note]  
> Neue Windows Anwendungen sollten [Unicode](unicode.md) verwenden, um die Inkonsistenzen verschiedener Codepages zu vermeiden und die Lokalisierung zu vereinfachen.

 

Jede Codepage wird durch einen Codepagebezeichner dargestellt, z.B. 1252, und wird von den Unicode- und Zeichensatz-API-Funktionen verarbeitet. Eine Liste der unterstützten Codepagebezeichner finden Sie unter [Codepagebezeichner.](code-page-identifiers.md) Die Referenz "Code Pages" im Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) enthält vollständige Beschreibungen vieler Codepages.

Windows Codepages, die häufig als "ANSI-Codepages" bezeichnet werden, sind Codepages, für die Nicht-ASCII-Werte (Werte größer als 127) internationale Zeichen darstellen. Diese Codepages werden nativ in Windows Me verwendet und sind auch auf Windows NT und höher verfügbar.

> [!Note]  
> Ursprünglich basierte Windows Codepage 1252, die häufig für Englisch und andere westepäische Sprachen verwendet wird, auf einem Ansi-Entwurf (American National Standards Institute). Dieser Entwurf wurde schließlich ZU ISO 8859-1, aber Windows Codepage 1252 wurde implementiert, bevor der Standard endgültig wurde, und ist nicht identisch mit ISO 8859-1.

 

Viele Windows-API-Funktionen weisen die Versionen "A" (ANSI) und "W" (wide, Unicode) auf. Die Version "A" verarbeitet Text basierend auf Windows Codepages, während die Version "W" Unicode-Text verarbeitet. Weitere Informationen finden Sie [unter Windows Datentypen für Zeichenfolgen](windows-data-types-for-strings.md) und [Konventionen für Funktionsprototypen.](conventions-for-function-prototypes.md)

Windows Codepages werden manchmal auch als "aktive Codepages" oder "systemaktive Codepages" bezeichnet. Ein Windows Betriebssystem verfügt immer über eine derzeit aktive Windows Codepage. Alle [ANSI-Versionen von API-Funktionen](conventions-for-function-prototypes.md) verwenden die derzeit aktive Codepage.

OEM-Codepages (Original Equipment Manufacturer) sind Codepages, für die Nicht-ASCII-Werte Zeichen für Linienzeichnung und Interpunktionszeichen darstellen. Diese Codepages wurden ursprünglich für MS-DOS verwendet und werden weiterhin für Konsolenanwendungen verwendet. Sie werden auch für die nicht erweiterten Dateinamen in den Dateisystemen FAT12, FAT16 und FAT32 verwendet, wie unter [In Dateinamen verwendete Zeichensätze](character-sets-used-in-file-names.md)beschrieben. Die übliche OEM-Codepage für Englisch ist Die Codepage 437.

Sowohl für Windows Codepages als auch für OEM-Codepages entsprechen die code-Werte, die über 0x7F 0x00 werden, dem 7-Bit-ASCII-Zeichensatz. Codewerte, die über 0x19 und 0x7F 0x00 werden, stellen immer standardisierte Steuerzeichen und 0x20 bis 0x7E standardisierte anzeigebare Zeichen dar. Zeichen, die durch die verbleibenden Codes dargestellt werden, 0x80 0xff, variieren je nach Zeichensatz. Jeder Zeichensatz enthält verschiedene Sonderzeichen, die in der Regel für eine Sprache oder Eine Gruppe von Sprachen angepasst werden. Windows Codepage 1252 und OEM-Codepage 437 werden im Allgemeinen in der USA verwendet.

Zusätzlich zu Windows und OEM-Codepages können Ihre Anwendungen nicht native Codepages verwenden. Beispiele hierfür sind EBCDIC- und Macintosh-Codepages.

Zwei Unicode-Codierungen (UTF-7 und UTF-8) werden als Codepages implementiert. Wie andere Codepages ist jede Seite durch einen numerischen Bezeichner bekannt und kann mit vielen der gleichen Unicode- und Zeichensatz-API-Funktionen verarbeitet werden.

Codepages können entweder [SBCS-Seiten (Single-Byte Character Set)](single-byte-character-sets.md) oder [Doppel-Byte-Seiten](double-byte-character-sets.md) (DBCS) sein. Auf SBCS-Seiten codiert jedes Byte direkt ein einzelnes Zeichen, sodass genau 256 unterschiedliche Zeichen (einschließlich Steuerzeichen, Buchstaben, Ziffern, Satzzeichen, Symbolen und ähnlichem) dargestellt werden können. DBCS-Codepages werden für Sprachen wie Japanisch und Chinesisch verwendet. Auf einer solchen Codepage weisen einige Zeichen 2-Byte-Codierungen mit bestimmten Bytewerten (immer Werte größer als 127) auf, die als "Leadbytes" dienen. Anstatt Zeichen selbst zu codieren, können Leadbytes nur in Verbindung mit einem "nachgestellten Byte" einem Zeichen zugeordnet werden.

Einige Legacyprotokolle erfordern die Verwendung von SBCS- und DBCS-Codepages. Jede SBCS-/DBCS-Codepage unterstützt unterschiedliche Zeichen, aber keine Codepage unterstützt die gesamte Bandbreite von Zeichen, die von Unicode bereitgestellt werden. Jede SBCS/DBCS-Codepage unterstützt eine andere Teilmenge, die unterschiedlich codiert ist.

> [!Note]  
> Daten, die von einer SBCS- oder DBCS-Codepage in eine andere konvertiert werden, sind beschädigt, da der gleiche Datenwert auf verschiedenen Codepages ein anderes Zeichen codieren kann. Daten, die aus Unicode in SBCS oder DBCS konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes Zeichen darstellen kann, das in diesen bestimmten Unicode-Daten verwendet wird.

 

Zusätzlich zu den SBCS- und DBCS-Codepages verfügen Ihre Anwendungen über die Multibyte-Zeichensatz-Codepages 52936, 54936, 51949 und 5022x, die einen ähnlichen Ansatz wie bei einem DBCS verwenden. Eine Multibyte-Zeichensatz-Codepage geht jedoch über die 2-Byte-Codierung einiger Zeichen hinaus. UTF-7 und UTF-8 verwenden einen ähnlichen Ansatz zum Codieren von Unicode basierend auf 7-Bit- bzw. 8-Bit-Bytes. Weitere Informationen finden Sie unter [Unicode.](unicode.md)

Mehrere Unicode- und Zeichensatzfunktionen ermöglichen Es Ihren Anwendungen, Codepages zu verarbeiten. Eine Anwendung kann die Funktionen [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) und [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) verwenden, um Informationen zu einer Codepage abzurufen. Diese Informationen enthalten das Standardzeichen, das verwendet wird, wenn ein Zeichen in einer konvertierten Zeichenfolge keinen entsprechenden Eintrag auf der Codepage enthält.

Eine Anwendung kann die Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwenden, um Zeichenfolgen basierend auf Windows Codepages und Unicode-Zeichenfolgen zu konvertieren. Obwohl ihre Namen auf "MultiByte" verweisen, funktionieren diese Funktionen gleichermaßen gut mit SBCS-, DBCS- und Multibyte-Zeichensatz-Codepages.

> [!Note]  
> [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) kann einige Daten verlieren, wenn die angegebene Codepage nicht alle Zeichen in einer Unicode-Zeichenfolge darstellen kann.

 

Ihre Anwendung kann mithilfe der standardmäßigen C-Laufzeitbibliotheksfunktionen zwischen Windows Codepages und OEM-Codepages konvertieren. Die Verwendung dieser Funktionen birgt jedoch das Risiko eines Datenverlusts, da die Zeichen, die von jeder Codepage dargestellt werden können, nicht genau übereinstimmen.

Ihre Anwendungen können auch die [**GetACP-Funktion**](/windows/desktop/api/Winnls/nf-winnls-getacp) aufrufen. Diese Funktion ruft den Bezeichner der aktuellen CODEPAGE Windows (ANSI) ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> </dl>

 

 



