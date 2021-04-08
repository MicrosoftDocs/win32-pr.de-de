---
description: Ein Registrierungs Wert kann Daten in verschiedenen Formaten speichern.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Registrierungs Werttypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc653e69c514bc77323704485e88f0a57eebaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865700"
---
# <a name="registry-value-types"></a>Registrierungs Werttypen

Ein Registrierungs Wert kann Daten in verschiedenen Formaten speichern. Wenn Sie Daten unter einem Registrierungs Wert speichern, indem Sie beispielsweise die [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) -Funktion aufrufen, können Sie einen der folgenden Werte angeben, um den Typ der gespeicherten Daten anzugeben. Wenn Sie einen Registrierungs Wert abrufen, verwenden Funktionen wie [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) diese Werte, um den Typ der abgerufenen Daten anzugeben.

Die folgenden Registrierungs Werttypen sind in "Winnt. h" definiert.



| Wert                                 | type                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG- \_ Binärdatei<br/>                | Binärdaten in beliebiger Form.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| REG \_ DWORD<br/>                 | Eine 32-Bit-Zahl.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ DWORD \_ Little- \_ umdian<br/> | Eine 32-Bit-Zahl im Little-Endian-Format.<br/> Windows ist für die unter Führung in Little-Endian-Computerarchitekturen konzipiert. Daher wird dieser Wert \_ in den Windows-Header Dateien als "reg DWORD" definiert.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD Big-DWORD \_ \_<br/>    | Eine 32-Bit-Zahl im Big-Endian-Format.<br/> Einige Unix-Systeme unterstützen Big-d-Architekturen.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ Expand \_ SZ<br/>            | Eine auf NULL endenden Zeichenfolge, die nicht erweiterte Verweise auf Umgebungsvariablen (z. b. "% Path%") enthält. Es handelt sich um eine Unicode-oder ANSI-Zeichenfolge, je nachdem, ob Sie die Unicode-oder ANSI-Funktionen verwenden. Um die Umgebungsvariablen Verweise zu erweitern, verwenden Sie die [**expandenvironment Strings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) -Funktion.<br/>                                                                                 |
| REG- \_ Link<br/>                  | Eine NULL-terminierte Unicode-Zeichenfolge, die den Zielpfad eines symbolischen Links enthält, der durch Aufrufen der [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) -Funktion mit der reg- \_ Option \_ Create Link erstellt wurde \_ .<br/>                                                                                                                                                                                                                          |
| REG \_ \_ MultiSZ<br/>             | Eine Sequenz von null-terminierten Zeichen folgen, die durch eine leere Zeichenfolge ( \\ 0) beendet wird.<br/> Es folgt ein Beispiel:<br/> *Zeichenfolge1* \\ 0 *Zeichenfolge2* \\ 0 *string3* \\ 0 *laststring* \\ 0 \\ 0<br/> Die erste \\ 0 beendet die erste Zeichenfolge, die zweite bis die letzte \\ 0 beendet die letzte Zeichenfolge, und die letzte \\ 0 beendet die Sequenz. Beachten Sie, dass das abschließende Abschluss Zeichen in die Länge der Zeichenfolge einbezogen werden muss.<br/> |
| REG \_ None<br/>                  | Kein definierter Werttyp.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| REG \_ QWORD<br/>                 | Eine 64-Bit-Zahl.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWORD \_ Little- \_ umdian<br/> | Eine 64-Bit-Zahl im Little-Endian-Format.<br/> Windows ist für die unter Führung in Little-Endian-Computerarchitekturen konzipiert. Daher wird dieser Wert \_ in den Windows-Header Dateien als "reg QWORD" definiert.<br/>                                                                                                                                                                                                                          |
| REG- \_ SZ<br/>                    | Eine NULL-terminierte Zeichenfolge. Dies ist entweder eine Unicode-oder eine ANSI-Zeichenfolge, je nachdem, ob Sie die Unicode-oder ANSI-Funktionen verwenden.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Zeichenfolgenwerte

Wenn die Daten den Typ "reg \_ SZ", "reg \_ \_ MultiSZ" oder "reg \_ Expand SZ" \_ aufweisen, wurde die Zeichenfolge möglicherweise nicht mit den ordnungsgemäßen abschließenden NULL-Zeichen gespeichert. Wenn Sie daher eine Zeichenfolge aus der Registrierung lesen, müssen Sie sicherstellen, dass die Zeichenfolge ordnungsgemäß beendet wird, bevor Sie Sie verwenden. Andernfalls wird möglicherweise ein Puffer überschrieben. (Beachten Sie, dass reg \_ MultiSZ- \_ Zeichen folgen müssen zwei abschließende Null-Zeichen enthalten.)

Wenn Sie eine Zeichenfolge in die Registrierung schreiben, müssen Sie die Länge der Zeichenfolge angeben, einschließlich des abschließenden NULL-Zeichens ( \\ 0). Ein häufiger Fehler ist die Verwendung der Funktion " **strinlen** ", um die Länge der Zeichenfolge zu bestimmen, jedoch zu vergessen, dass " **straulen** " nur die Anzahl der Zeichen in der Zeichenfolge zurückgibt, ohne das abschließende Null Zeichen. Daher sollte die Länge der Zeichenfolge wie folgt berechnet werden: `strlen( string ) + 1`

Eine reg \_ \_ MultiSZ-Zeichenfolge endet mit einer Zeichenfolge mit der Länge 0. Aus diesem Grund ist es nicht möglich, eine Zeichenfolge der Länge 0 (null) in die Sequenz einzufügen. Eine leere Sequenz wird wie folgt definiert: \\ 0.

Im folgenden Beispiel wird eine reg \_ \_ MultiSZ-Zeichenfolge durchlaufen.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void SampleSzz(PTSTR pszz)
{
   _tprintf(_TEXT("\tBegin multi-sz string\n"));
   while (*pszz) 
   {
      _tprintf(_TEXT("\t\t%s\n"), pszz);
      pszz = pszz + _tcslen(pszz) + 1;
   }
   _tprintf(_TEXT("\tEnd multi-sz\n"));
}

int __cdecl main(int argc, char **argv)
{
   // Because the compiler adds a \0 at the end of quoted strings, 
   // there are two \0 terminators at the end. 

   _tprintf(_TEXT("Conventional multi-sz string:\n"));  
   SampleSzz(_TEXT("String1\0String2\0String3\0LastString\0"));

   _tprintf(_TEXT("\nTest case with no strings:\n"));  
   SampleSzz(_TEXT(""));

   return 0;
}
```



## <a name="byte-formats"></a>Byte Formate

Im *Little-Endian-Format* wird ein Multi-Byte-Wert im Arbeitsspeicher vom niedrigsten Byte (dem "kleinen Ende") bis zum höchsten Byte gespeichert. Beispielsweise wird der Wert 0x12345678 als (0x78 0x56 0x34 0x12) im Little-Endian-Format gespeichert.

Im *Big-Endian-Format* wird ein Multi-Byte-Wert im Arbeitsspeicher vom höchsten Byte (dem "großen Ende") bis zum niedrigsten Byte gespeichert. Beispielsweise wird der Wert 0x12345678 als (0x12 0x34 0x56 0x78) im Big-Endian-Format gespeichert.

 

