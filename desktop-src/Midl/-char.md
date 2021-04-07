---
title: /char-Schalter
description: Mithilfe des/Char-Schalters können Sie sicherstellen, dass der Mittelwert Compiler und der C-Compiler ordnungsgemäß für alle char-und Small-Typen funktionieren.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718702"
---
# <a name="char-switch"></a>/char-Schalter

Mithilfe des **/char** -Schalters können Sie sicherstellen, dass der Mittelwert Compiler und der C-Compiler ordnungsgemäß für alle [**char**](char-idl.md) -und [**Small**](small.md) -Typen funktionieren.

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>signiert * * * *


</dt> <dd>

Gibt an, dass der C-Compiler-Standard Typ für [**char**](char-idl.md) signiert ist. Alle Vorkommen von **char** , die nicht von einer Vorzeichen Spezifikation begleitet werden, werden als unsigniertes char generiert.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>nicht signiert * * * *


</dt> <dd>

Gibt an, dass der Standard-C-Compilertyp für [**char**](char-idl.md) nicht signiert ist. Alle Verwendungszwecke von [**Small**](small.md) , die nicht von einer Signierungs Spezifikation begleitet werden, werden als klein signiert generiert.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ASCII7 * * * *


</dt> <dd>

Gibt an, dass alle [**char**](char-idl.md) -Werte ohne bestimmtes Signierungs Schlüsselwort an die generierten Dateien übermittelt werden sollen. Alle Verwendungszwecke von " [**Small**](small.md) ", die nicht von einer Vorzeichen Spezifikation begleitet werden, werden als **klein** generiert.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Definitions [**gemäß ist "**](char-idl.md) Mittelwert Zeichen" nicht signiert. "Small" ist im Hinblick auf **char** ( \# define Small Char) und in der Mitte [**Small**](small.md) signiert.

Der **/char** -Schalter weist den Mittelwert Compiler an, explizite [**signierte**](signed.md) oder [**unsignierte**](unsigned.md) Deklarationen in den generierten Dateien anzugeben, wenn die C-compilersignier Deklaration mit dem Standardwert für diesen Typ in Konflikt steht.

Beachten Sie, dass der mittlerer l-Compiler die Stub als C-Quellcode generiert, den Sie als Teil der Client-und Serverprogramme kompilieren müssen. Einige Compiler verwenden eine **signierte char** Everywhere [**-**](char-idl.md) Daten, die im Quellcode angegeben sind. Der stubquellcode, den der Mittell-Compiler generiert, behandelt alle **char** -Daten als **unsigniertes char**. Wenn der Mittell-Compiler einfach alle **char** -Daten in der IDL-Datei als **char** -Daten in den Stubs generiert hat, verursachen Compiler, die ein **signiertes char** für **char** -Daten verwenden, einen Konflikt im stubquellcode.

Der Zweck des Befehls Zeilenschalters **/char** besteht darin, diese potenziellen Konflikte zu beheben. Alle Daten, die als " [**char**](char-idl.md) " in der IDL-Datei angegeben sind, werden im stubquellcode als **Ganzzahl ohne Vorzeichen char** -Zeichen beibehalten. Außerdem werden [**kleine**](small.md) Daten als signiert verwaltet.

In der folgenden Tabelle werden die generierten Typen zusammengefasst.



| Mittel l/char (Option)       | Generierter char-Typ | Generierter kleiner Typ |
|-------------------------|---------------------|----------------------|
| **Mittel l/char signiert**   | **unsigned char**   | **small**            |
| **Mittel l/char unsigniert** | **char**            | **klein signiert**     |
| **Mittel l/char ASCII7**   | **char**            | **small**            |



 

Die Option **/char** signed gibt an, dass der C-Compiler char und Small Typen signiert sind. Damit die mittlere Standardeinstellung für **char** gefunden werden kann, muss der-compilercompiler alle Verwendungszwecke von **char** konvertieren, die nicht von einer **Signierungs** Spezifikation in ein Zeichen ohne Vorzeichen begleitet werden. Der [**kleine**](small.md) Typ wird nicht geändert, da dieser C-Compiler-Standard für **Small** mit dem mittleren Standardwert übereinstimmt.

Die Option **/char** Ganzzahl ohne Vorzeichen gibt an, dass der C-Compiler- [**char**](char-idl.md) -Typ nicht signiert ist. Der-compilercompiler konvertiert alle Verwendungszwecke von [**Small**](small.md) , nicht von einer Vorzeichen Spezifikation in eine **klein** **signierte** .

Die ASCII7-Option gibt an, dass [**char**](char-idl.md) -Typen keine explizite Signierungs Spezifikation hinzugefügt wird. Der Typ [**Small**](small.md) wird als **kleiner** generiert.

Um Verwirrung zu vermeiden, sollten Sie nach Möglichkeit explizite Vorzeichen Spezifikationen für [**char**](char-idl.md) und Small types in der IDL-Datei verwenden. Beachten Sie, dass die Verwendung explizit signierter **char** -Typen in ihrer IDL-Datei von DCE IDL nicht unterstützt wird. Diese Funktion ist daher nicht verfügbar, wenn Sie mit dem [**/OSF**](-osf.md) -Schalter für mittlere Kompilierung kompilieren.

Weitere Informationen zu **/char** finden Sie unter [**Small**](small.md).

## <a name="examples"></a>Beispiele

**Mittel l/char signierte Datei Name. idl**

**Mittel l/char Dateiname. idl ohne Vorzeichen**

**Mittel l/char ASCII7 filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**zuletzt**](small.md)
</dt> </dl>

 

 




