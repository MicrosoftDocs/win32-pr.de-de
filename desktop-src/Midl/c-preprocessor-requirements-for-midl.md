---
title: C-präprozessoranforderungen für die Mittel l
description: Diese Seite gilt nur für Entwickler, die bestimmte Gründe dafür haben, den Microsoft C/C++-Präprozessor als Präprozessor zu ersetzen, der von der Mittell verwendet wird, oder für Entwickler, die angepasste präprozessorswitches angeben müssen.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- Mittlere compilermittell, C-präprozessoranforderungen
- C-präprozessormittell, Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947943"
---
# <a name="c-preprocessor-requirements-for-midl"></a>C-präprozessoranforderungen für die Mittel l

Diese Seite gilt nur für Entwickler, die bestimmte Gründe dafür haben, den Microsoft C/C++-Präprozessor als Präprozessor zu ersetzen, der von der Mittell verwendet wird, oder für Entwickler, die angepasste präprozessorswitches angeben müssen. Die mittleren Schalter [**/cpp \_ cmd**](-cpp-cmd.md), [**/cpp \_ opt**](-cpp-opt.md)und [**/No \_ cpp**](-no-cpp-nocpp.md) werden verwendet, um das Standardverhalten des Compilers zu überschreiben. Es gibt in der Regel keinen Grund, den Microsoft C/C++-Präprozessor zu ersetzen und keine angepassten präprozessorschalter anzugeben.

Der mittlerer l-Compiler verwendet bei der anfänglichen Verarbeitung der IDL-Datei einen C-Präprozessor. Die Buildumgebung, die beim Kompilieren der IDL-Dateien verwendet wird, ist einem Standard-C/C++-Präprozessor zugeordnet. Wenn ein anderer Präprozessor verwendet werden soll, aktiviert der Mittell-Compilerschalter [**/cpp \_ cmd**](-cpp-cmd.md) eine außer Kraft setzung des standardmäßigen C/C++-präprozessornamens:

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*\_präprozessorname*
</dt> <dd>

Gibt den Namen des präprozessornamens an, der von der Mittell verwendet werden soll. Kann mit einem Pfad zur Binärdatei angegeben werden. Die Erweiterung ". exe" ist optional.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Gibt den Namen der IDL-Datei an.

</dd> </dl>

-   Der mittlerer l-Compiler erwartet, dass der Präprozessor die folgenden Konventionen beachtet:
-   Die Eingabedatei wird als letztes Argument in der Befehlszeile angegeben.
-   Der Präprozessor muss die Ausgabe an das Standardausgabe Gerät (stdout) umleiten.
-   Im Ausgabestream des Präprozessors sind die **\# Zeilen** Anweisungen vorhanden, um bessere Diagnosemeldungen zu ermöglichen.
-   Die Zeilen Direktiven sind die einzigen Präprozessordirektiven im Ausgabestream.

In der Mitte wird davon ausgegangen, dass der erzeugte Präprozessor alle Präprozessordirektiven aus dem Eingabestream des Compilers entfernt hat, mit Ausnahme des Auftretens der Zeilen Direktive, die zum Ermitteln des Quell Speicher Orts in compilernachrichten erforderlich ist. Wenn ein vom Microsoft C/C++-Präprozessor abweichender Präprozessor oder Präprozessoroptionen mit dem [**/cpp \_ opt**](-cpp-opt.md) -Schalter angegeben werden, ist die Angabe einer entsprechenden Präprozessoroption erforderlich, die die Zeilen Direktiven in den Eingabestream des Compilers einfügt. Für den Microsoft C/C++-Präprozessor müsste z. b. die **/E** -Option verwendet werden:

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

Die **\# Line** -Direktive wird von der mittleren l in einer der folgenden Formen akzeptiert:

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

Eine umfassende Beschreibung der line-Direktive und anderer Präprozessordirektiven finden Sie in der Dokumentation für den verwendeten C-Compiler.

In der-Klasse wird nur die Zeilen Präprozessordirektive akzeptiert. Wenn der/No- [**\_ cpp**](-no-cpp-nocpp.md) -Schalter verwendet wird, darf die Eingabedatei nicht über andere Präprozessordirektiven verfügen, oder die Eingabedatei muss vor dem Aufrufen von "Mittel l" verarbeitet werden.

Weitere Informationen finden Sie unter [Umgang mit \# Definitionen in IDL-Dateien](dealing-with-defines-in-idl-files-2.md).

 

 




