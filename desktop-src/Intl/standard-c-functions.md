---
description: Die C-Standardlaufzeitbibliotheken enthalten sowohl Unicode-UTF-16-Versionen (Breitzeichen) von Zeichenfolgenfunktionen, die mit Unicode und byteorientierten Versionen von Zeichenfolgenfunktionen verwendet werden können, die mit Zeichen aus Single-Byte-Zeichensätzen (Single-Byte Character Sets, SBCSs) verwendet werden können. Der Unicode-Datentyp WCHAR ist mit dem Datentyp wchar t in ANSI C kompatibel und ermöglicht den Zugriff \_ auf die Unicode-Zeichenfolgenfunktionen. Die Unicode-Versionen der Funktionen beginnen mit den Buchstaben \# &0034;wcs&\# 0034; (oder manchmal &\# 0034; \_ wcs&\# 0034;). Der für Codepages verwendete Datentyp CHAR ist mit dem Zeichendatentyp char in ANSI C kompatibel, um den Zugriff auf die Zeichenfolgenfunktionen zu ermöglichen. Die Zeichenversionen der Funktionen beginnen mit den Buchstaben \# &0034;str&\# 0034;. Es gibt auch Sonderversionen für Doppel-Byte-Zeichensätze (Double-Byte Character Sets, DBCSs), die mit den Buchstaben &\# 0034 beginnen. \_ mbs&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: C-Standardfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e576dd8ad506d3d0f3379c161526dd7b9330542ca1cc575c95e3eda8e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130160"
---
# <a name="standard-c-functions"></a>C-Standardfunktionen

Die C-Standardlaufzeitbibliotheken enthalten sowohl Unicode-UTF-16-Versionen (Breitzeichen) von Zeichenfolgenfunktionen, die mit [Unicode](unicode.md) und byteorientierten Versionen von Zeichenfolgenfunktionen verwendet werden können, die mit Zeichen aus [Single-Byte-Zeichensätzen (Single-Byte](single-byte-character-sets.md) Character Sets, SBCSs) verwendet werden können. Der Unicode-Datentyp WCHAR ist mit dem Datentyp wchar t in ANSI C kompatibel und ermöglicht den Zugriff \_ auf die Unicode-Zeichenfolgenfunktionen. Die Unicode-Versionen der Funktionen beginnen mit den Buchstaben "wcs" (oder manchmal \_ "wcs"). Der für Codepages verwendete Datentyp CHAR ist mit dem Zeichendatentyp char in ANSI C kompatibel, um den Zugriff auf die Zeichenfolgenfunktionen zu ermöglichen. Die Zeichenversionen der Funktionen beginnen mit den Buchstaben "str". Es gibt auch spezielle Versionen für [Doppelbyte-Zeichensätze (Double-Byte Character Sets,](double-byte-character-sets.md) DBCSs), die mit den Buchstaben \_ "mbs" beginnen.

Die C-Standardlaufzeitbibliotheken enthalten generische Funktionen für alle standardmäßigen C-Zeichenfolgenfunktionen. Sie beginnen mit \_ "tcs" und werden in der Headerdatei Tchar.h aufgeführt. Diese Funktionen verwenden den generischen TCHAR-Datentyp.

Eine Anwendung muss die folgenden Zeilen hinzufügen, um die generischen Funktionen zu verwenden und für Unicode zu kompilieren.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Beachten Sie, dass sowohl die Dateien Tchar.h als auch Wchar.h erforderlich sind und dass auch der führende Unterstrich für die \_ UNICODE-Variable erforderlich ist. Diese Nomenklatur ist spezifisch für die C-Standardbibliothek. "UNICODE", das ohne Unterstrich gerendert wird, ist für die Microsoft Windows Runtimes.

Die [funktionen wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) und [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) können aus dem zeichensatz, der von der C-Standardbibliothek unterstützt wird, mit einigen Einschränkungen in Unicode und zurück konvertieren. Weitere Informationen zum Übersetzen von Zeichenfolgen in und aus Unicode finden Sie unter [Übersetzung zwischen Zeichenfolgentypen.](translation-between-string-types.md)

Die in Tchar.h definierte [printf-Funktion](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) unterstützt die gleichen Formatspezifikationen wie die Strsafe.h-Druckfunktionen, z.B. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa). Auf ähnliche Weise definiert Tchar.h eine [wprintf-Funktion,](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) bei der die Formatzeichenfolge selbst eine Unicode-Zeichenfolge ist.

> [!Caution]  
> Eine schlechte Pufferbehandlung ist in vielen Sicherheitsproblemen mit Pufferüberläufen zu sehen. Weitere Informationen [finden Sie unter Strsafe.h Reference (Strsafe.h-Referenz).](../menurc/strsafe-ovw.md) Die in Strsafe.h definierten Funktionen bieten zusätzliche Verarbeitung für die richtige Pufferbehandlung in Ihrem Code. Sie sollen ihre integrierten C/C++-Entsprechungen sowie bestimmte Microsoft Windows ersetzen. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
