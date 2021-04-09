---
description: Die standardmäßigen C-Laufzeitbibliotheken enthalten beide Unicode-UTF-16-Versionen (breit Zeichen) von Zeichen folgen Funktionen, die mit Unicode-und Byte orientierten Versionen von Zeichen folgen Funktionen verwendet werden können, die mit Zeichen aus Einzel Byte-Zeichensätzen (SBCSs) verwendet werden können. Der Unicode-Datentyp WCHAR ist mit dem-Datentyp WCHAR \_ t in ANSI C kompatibel und ermöglicht den Zugriff auf die Unicode-Zeichen folgen Funktionen. Die Unicode-Versionen der Funktionen beginnen mit den Buchstaben &\# 0034; WCS&\# 0034; (oder manchmal &\# 0034; \_ WCS-&\# 0034;). Der für Codepages verwendete Datentyp char ist mit dem Zeichen Datentyp char in ANSI C kompatibel, um den Zugriff auf die Zeichen folgen Funktionen zu ermöglichen. Die Zeichen Versionen der Funktionen beginnen mit den Buchstaben &\# 0034; Str&\# 0034;. Es gibt auch spezielle Versionen für Doppelbyte-Zeichensätze (dbcss), die mit den Buchstaben &\# 0034; beginnen. \_ MSB&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Standard-C-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868904"
---
# <a name="standard-c-functions"></a>Standard-C-Funktionen

Die standardmäßigen C-Laufzeitbibliotheken enthalten beide Unicode-UTF-16-Versionen (breit Zeichen) von Zeichen folgen Funktionen, die mit [Unicode](unicode.md) -und Byte orientierten Versionen von Zeichen folgen Funktionen verwendet werden können, die mit Zeichen aus [Einzel Byte-Zeichensätzen](single-byte-character-sets.md) (SBCSs) verwendet werden können. Der Unicode-Datentyp WCHAR ist mit dem-Datentyp WCHAR \_ t in ANSI C kompatibel und ermöglicht den Zugriff auf die Unicode-Zeichen folgen Funktionen. Die Unicode-Versionen der Funktionen beginnen mit den Buchstaben "WCS" (oder manchmal " \_ WCS"). Der für Codepages verwendete Datentyp char ist mit dem Zeichen Datentyp char in ANSI C kompatibel, um den Zugriff auf die Zeichen folgen Funktionen zu ermöglichen. Die Zeichen Versionen der Funktionen beginnen mit den Buchstaben "str". Es gibt auch spezielle Versionen für [Doppelbyte-Zeichensätze](double-byte-character-sets.md) (dbcss), die mit den Buchstaben " \_ MSB" beginnen.

Die standardmäßigen c-Laufzeitbibliotheken enthalten generische Funktionen für alle Standard-c-Zeichen folgen Funktionen. Sie beginnen mit " \_ TCS" und sind in der Header Datei "Tchar. h" aufgeführt. Diese Funktionen verwenden den generischen TCHAR-Datentyp.

Eine Anwendung muss die folgenden Zeilen hinzufügen, um die generischen Funktionen zu verwenden und für Unicode zu kompilieren.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Beachten Sie, dass die Dateien "Tchar. h" und "WCHAR. h" erforderlich sind und dass der führende Unterstrich für die \_ Unicode-Variable ebenfalls erforderlich ist. Diese Nomenklatur ist spezifisch für die Standard-C-Bibliothek. "Unicode", die ohne Unterstrich gerendert wird, ist für die Microsoft Windows-Laufzeiten.

Die Funktionen [wcstomsb](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) und [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) können mit einigen Einschränkungen aus dem von der Standard-C-Bibliothek unterstützten Zeichensatz in Unicode und Back konvertiert werden. Weitere Informationen zum Übersetzen von Zeichen folgen in und aus Unicode finden Sie unter [Übersetzung zwischen Zeichen folgen Typen](translation-between-string-types.md).

Die in Tchar. h definierte [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) -Funktion unterstützt die gleichen Formatspezifikationen wie die "strausafe. h"-Druckfunktionen, z. b. " [**stringcbprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)". Ebenso definiert Tchar. h eine [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) -Funktion, in der die Format Zeichenfolge selbst eine Unicode-Zeichenfolge ist.

> [!Caution]  
> Eine schlechte Puffer Behandlung ist in vielen Sicherheitsproblemen enthalten, die Pufferüberläufe einschließen. Weitere Informationen finden Sie unter [Referenz](../menurc/strsafe-ovw.md)zu "" Die in "strausafe. h" definierten Funktionen bieten zusätzliche Verarbeitungsschritte für die ordnungsgemäße Puffer Behandlung in Ihrem Code. Sie sind dazu gedacht, Ihre integrierten C/C++-Gegenstücke und bestimmte Microsoft Windows-Implementierungen zu ersetzen. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
