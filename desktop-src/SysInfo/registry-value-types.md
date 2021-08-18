---
description: Ein Registrierungswert kann Daten in verschiedenen Formaten speichern.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Registrierungswerttypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2bc73e03d9aab8d39bdda31ab308af1749f22315a262ceb4ae28ec743c8c69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885013"
---
# <a name="registry-value-types"></a>Registrierungswerttypen

Ein Registrierungswert kann Daten in verschiedenen Formaten speichern. Wenn Sie Daten unter einem Registrierungswert speichern, z. B. durch Aufrufen der [**RegSetValueEx-Funktion,**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) können Sie einen der folgenden Werte angeben, um den Typ der zu speichernden Daten anzugeben. Wenn Sie einen Registrierungswert abrufen, verwenden Funktionen wie [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) diese Werte, um den Typ der abgerufenen Daten anzugeben.

Die folgenden Registrierungswerttypen werden in Winnt.h definiert.



| Wert                                 | type                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ BINARY<br/>                | Binärdaten in beliebiger Form.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| REG \_ DWORD<br/>                 | Eine 32-Bit-Zahl.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ DWORD \_ LITTLE \_ ENDIAN<br/> | Eine 32-Bit-Zahl im Little-Endian-Format.<br/> Windows ist für die Ausführung auf Little-Endian-Computerarchitekturen konzipiert. Daher wird dieser Wert in den Headerdateien als REG \_ DWORD Windows definiert.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ BIG \_ ENDIAN<br/>    | Eine 32-Bit-Zahl im Big-Endian-Format.<br/> Einige UNIX unterstützen Big-Endian-Architekturen.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ EXPAND \_ SZ<br/>            | Eine auf NULL beendete Zeichenfolge, die nicht vorhandene Verweise auf Umgebungsvariablen enthält (z. B. "%PATH%"). Es wird eine Unicode- oder ANSI-Zeichenfolge sein, je nachdem, ob Sie die Unicode- oder ANSI-Funktionen verwenden. Verwenden Sie die Funktion [**ExpandEnvironmentStrings, um die Umgebungsvariablenverweise zu**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) erweitern.<br/>                                                                                 |
| REG \_ LINK<br/>                  | Eine auf NULL beendete Unicode-Zeichenfolge, die den Zielpfad einer symbolischen Verknüpfung enthält, die durch Aufrufen der [**RegCreateKeyEx-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) mit REG \_ OPTION CREATE LINK erstellt \_ \_ wurde.<br/>                                                                                                                                                                                                                          |
| REG \_ MULTI \_ SZ<br/>             | Eine Sequenz von auf NULL beendeten Zeichenfolgen, die durch eine leere Zeichenfolge ( \\ 0) beendet werden.<br/> Es folgt ein Beispiel:<br/> *String1* \\ 0 *String2* \\ 0 *String3* \\ 0 *LastString* \\ 0 \\ 0<br/> Die erste 0 beendet die erste Zeichenfolge, die zweite bis die letzte 0 die letzte Zeichenfolge und die letzte \\ \\ \\ 0 beendet die Sequenz. Beachten Sie, dass das endgültige Abschlusszeichen in die Länge der Zeichenfolge berücksichtigt werden muss.<br/> |
| REG \_ NONE<br/>                  | Kein definierter Werttyp.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| REG \_ QWORD<br/>                 | Eine 64-Bit-Zahl.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWORD \_ LITTLE \_ ENDIAN<br/> | Eine 64-Bit-Zahl im Little-Endian-Format.<br/> Windows ist für die Ausführung auf Little-Endian-Computerarchitekturen konzipiert. Daher wird dieser Wert als REG \_ QWORD in den Windows definiert.<br/>                                                                                                                                                                                                                          |
| REG \_ SZ<br/>                    | Eine NULL-terminierte Zeichenfolge. Dies ist entweder eine Unicode- oder eine ANSI-Zeichenfolge, je nachdem, ob Sie die Unicode- oder ANSI-Funktionen verwenden.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Zeichenfolgenwerte

Wenn Daten den Reg SZ-, REG MULTI SZ- oder REG EXPAND SZ-Typ haben, wurde die Zeichenfolge möglicherweise nicht mit den richtigen endenden \_ \_ \_ \_ \_ NULL-Zeichen gespeichert. Daher müssen Sie beim Lesen einer Zeichenfolge aus der Registrierung sicherstellen, dass die Zeichenfolge ordnungsgemäß beendet wird, bevor Sie sie verwenden. Andernfalls wird möglicherweise ein Puffer überschrieben. (Beachten Sie, dass REG \_ MULTI \_ SZ-Zeichenfolgen sollten zwei endende NULL-Zeichen enthalten.)

Wenn Sie eine Zeichenfolge in die Registrierung schreiben, müssen Sie die Länge der Zeichenfolge angeben, einschließlich des beendenden NULL-Zeichens ( \\ 0). Ein häufiger Fehler besteht in der Verwendung der **strlen-Funktion,** um die Länge der Zeichenfolge zu bestimmen, aber zu vergessen, dass **strlen** nur die Anzahl der Zeichen in der Zeichenfolge zurückgibt, ohne das beendende NULL-Zeichen ein. Daher sollte die Länge der Zeichenfolge wie folgt berechnet werden: `strlen( string ) + 1`

Eine REG \_ MULTI \_ SZ-Zeichenfolge endet mit einer Zeichenfolge der Länge 0. Daher ist es nicht möglich, eine Zeichenfolge der Länge 0 (null) in die Sequenz ein schließen. Eine leere Sequenz würde wie folgt definiert werden: \\ 0.

Im folgenden Beispiel wird eine REG \_ MULTI \_ SZ-Zeichenfolge durchgeschritten.


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



## <a name="byte-formats"></a>Byteformate

Im *Little-Endian-Format* wird ein Multi-Byte-Wert im Arbeitsspeicher vom niedrigsten Byte (das "little end") bis zum höchsten Byte gespeichert. Beispielsweise wird der Wert 0x12345678 als (0x78 0x56 0x34 0x12) im Little-Endian-Format gespeichert.

Im *Big-Endian-Format* wird ein Multi-Byte-Wert vom höchsten Byte (dem "big end") bis zum niedrigsten Byte im Arbeitsspeicher gespeichert. Beispielsweise wird der Wert 0x12345678 als (0x12 0x34 0x56 0x78) im Big-Endian-Format gespeichert.

 

