---
title: Importieren von Dateien und Typbibliotheken
description: Mit den mittleren Schlüsselwörtern "include", "Import" und "importlib" können Sie Code wieder verwenden, indem Sie auf vorhandene Header-, IDL-und ODL-Dateien (Object Definition Language) und kompilierte Typbibliotheken verweisen.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language mittlerer l, Aufgaben, Importieren von Dateien und Typbibliotheken
- Importieren der Mittell
- Typbibliotheken, Mittel l, importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353989"
---
# <a name="importing-files-and-type-libraries"></a>Importieren von Dateien und Typbibliotheken

Mit den mittleren Schlüsselwörtern " [**include**](include.md)", " [**Import**](import.md)" und " [**importlib**](importlib.md) " können Sie Code wieder verwenden, indem Sie auf vorhandene Header-, IDL-und ODL-Dateien (Object Definition Language) und kompilierte Typbibliotheken verweisen.

Mit der ACF [**include**](include.md) -Direktive können Sie in einer ACF-Datei eine oder mehrere C-sprach Header Dateien angeben, die in den in der Mitte generierten Stub-Code eingeschlossen werden sollen. Die generierte Datei enthält eine Zeile mit einer **\# include** -C-Präprozessordirektive mit der angezeigten Header Datei. Verwenden Sie diese **include** -Direktive zum Einbinden von Header Dateien, die für eine bestimmte Betriebsumgebung spezifisch sind und keine Informationen enthalten, die für die Schnittstelle zwischen Client und Server erforderlich sind. Verwenden Sie **include** nicht für Header Dateien, die Datentypen enthalten, die für die IDL-Datei verfügbar sein sollen. Verwenden Sie stattdessen die [**Import**](import.md) -Direktive.

## <a name="example-1"></a>Beispiel 1

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

Die IDL- [**Import**](import.md) Direktive ist die Standardmethode zum Übertragen von Typ-und Schnittstellendefinitionen aus anderen IDL-Dateien (oder ODL-Dateien) und Header Dateien in Ihre IDL-Datei. Alle IDL-Anweisungen in der importierten Datei (z. b. Typedefs, [**Konstante Deklarationen**](const.md) und Schnittstellendefinitionen) werden für die importierende IDL-Datei verfügbar.

Wie bei der Präprozessordirektive der C-Sprache weist die [**Import**](import.md) -Direktive den Compiler **\# an, Daten** Typen einzuschließen, die in den importierten IDL-Dateien definiert wurden. Anders als bei der **\# include** -Direktive ignoriert die **Import** -Direktive Prozedur Prototypen, da für Elemente in der importierten Datei keine Stubdaten generiert werden. Da der Präprozessor für die importierte Datei separat aufgerufen wird, werden Präprozessordirektiven (z. b. * *) nicht auf die importierende IDL-Datei übertragen.

Weitere Informationen zur Verwendung von [**Import**](import.md) zum Einschließen von System Header Dateien in eine IDL-Datei finden Sie unter [Importieren von System Header Dateien](importing-system-header-files.md).

## <a name="example-2"></a>Beispiel 2

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

Mit der ODL [**importlib**](importlib.md) -Direktive können Sie in ihrer IDL-oder ODL-Datei auf eine kompilierte Typbibliothek verweisen. Die **importlib** -Direktive muss sich in einer [**Library**](library.md) -Anweisung befinden und muss vor anderen Typbeschreibungen in der Bibliothek stehen. Die importierte Bibliothek und die generierte Bibliothek müssen zur Laufzeit für die Anwendung verfügbar sein.

## <a name="example-3"></a>Beispiel 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

Sie können auch die C-präprocessor **\# include** -Direktive verwenden, um Header und andere Dateien in Ihre IDL-oder ODL-Datei einzubeziehen. Beachten Sie jedoch, dass diese Direktive den gesamten Inhalt der angegebenen Datei enthält. Wenn eine Header Datei Prototypen enthält, die Sie in den von der Mitte generierten Stubdateien nicht benötigen oder verwenden möchten, oder wenn Sie nicht Remote fähige Typdefinitionen enthält, sollten Sie anstelle der **\# include** -Direktive die [**Import**](import.md) Direktive "Mittel l" verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Importieren**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**darunter**](include.md)
</dt> <dt>

[Importieren von System-Headerdateien](importing-system-header-files.md)
</dt> </dl>

 

 




