---
title: Importieren von Dateien und Typbibliotheken
description: Mit den MIDL-Schlüsselwörtern include, import und importlib können Sie Code wiederverwenden, indem Sie auf vorhandene Header-, IDL- und ODL-Dateien (Object Definition Language) und kompilierte Typbibliotheken verweisen.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language MIDL, Aufgaben, Importieren von Dateien und Typbibliotheken
- Importieren von MIDL
- Typbibliotheken MIDL , importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099ada5122ad024e342148bf3c453df0bd50872e6d59a2bbabd7d2892af5f93a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013738"
---
# <a name="importing-files-and-type-libraries"></a>Importieren von Dateien und Typbibliotheken

Mit den MIDL-Schlüsselwörtern [**,**](include.md) [**import**](import.md)und [**importlib**](importlib.md) können Sie Code wiederverwenden, indem Sie auf vorhandene Header-, IDL- und ODL-Dateien (Object Definition Language) und kompilierte Typbibliotheken verweisen.

Mit der [**Include-Direktive**](include.md) von ACF können Sie in einer ACF-Datei eine oder mehrere Headerdateien der C-Sprache angeben, die in den MIDL-generierten Stubcode eingeschlossen werden sollen. Die generierte Datei enthält eine Zeile mit einer **\# Include-C-Präprozessordi** direktive mit der angegebenen Headerdatei. Verwenden Sie diese include-Direktive, um Headerdateien zu verwenden, die für eine bestimmte Betriebsumgebung spezifisch sind und keine Informationen enthalten, die für die Schnittstelle zwischen Client und Server erforderlich sind.  Verwenden Sie include **nicht** für Headerdateien, die Datentypen enthalten, die für die IDL-Datei verfügbar sein sollten. Verwenden Sie stattdessen die [**Import-Direktive.**](import.md)

## <a name="example-1"></a>Beispiel 1

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

Die [**IDL-Import-Direktive**](import.md) ist die Standardmethode zum Importieren von Typ- und Schnittstellendefinitionen aus anderen IDL-Dateien (oder ODL)-Dateien und Headerdateien in Ihre IDL-Datei. Alle IDL-Anweisungen in der importierten Datei, z. B. Typedefs, const-Deklarationen und Schnittstellendefinitionen, werden für die importierende IDL-Datei verfügbar. [](const.md)

Wie die C-Sprach-Präprozessordi direktive **\# enthält,** weist die [**import-Direktive**](import.md) den Compiler an, Datentypen ein include, die in den importierten IDL-Dateien definiert wurden. Im Gegensatz **\# zur include-Direktive** ignoriert **die import-Direktive** Prozedurprototypen, da keine Stubs für etwas in der importierten Datei generiert werden. Da der Präprozessor für die importierte Datei separat aufgerufen wird, werden Präprozessordirektiven (z.B. **) nicht an die importierende IDL-Datei überträgt.

Weitere Informationen zur Verwendung von [**Import**](import.md) zum Ein- und Hinzufügen von Systemheaderdateien in eine IDL-Datei finden Sie unter [Importieren von Systemheaderdateien.](importing-system-header-files.md)

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

Mit der [**ODL-Importlib-Direktive**](importlib.md) können Sie auf eine kompilierte Typbibliothek in Ihrer IDL- oder ODL-Datei verweisen. Die **importlib-Direktive** muss sich in einer [**Bibliotheks-Anweisung**](library.md) und vor anderen Typbeschreibungen in der Bibliothek befindet. Die importierte Bibliothek sowie die generierte Bibliothek müssen zur Laufzeit für die Anwendung verfügbar sein.

## <a name="example-3"></a>Beispiel 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

Sie können auch die include-Direktive des C-Präprozessors verwenden, um Header und andere Dateien in Ihre IDL- oder ODL-Datei ein-/aus. **\#** Beachten Sie jedoch, dass diese Direktive den gesamten Inhalt der angegebenen Datei enthält. Wenn eine Headerdatei Prototypen enthält, die Sie in den MIDL-generierten Stubdateien nicht benötigen oder möchten, oder [](import.md) wenn sie nichtremotable Typdefinitionen enthält, sollten Sie die MIDL-Import-Direktive anstelle der **\# include-Direktive** verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**import**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**include**](include.md)
</dt> <dt>

[Importieren von System-Headerdateien](importing-system-header-files.md)
</dt> </dl>

 

 




