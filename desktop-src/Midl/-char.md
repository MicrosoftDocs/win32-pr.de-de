---
title: /char-Schalter
description: Mit dem Schalter /char können Sie sicherstellen, dass der MIDL-Compiler und der C-Compiler für alle char- und kleinen Typen ordnungsgemäß zusammenarbeiten.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char switch MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb459f7c2d6ff98a35e139cf07d9d95c4bed575e52b3d20258f570f07297943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963190"
---
# <a name="char-switch"></a>/char-Schalter

Mit **dem Schalter /char** können Sie sicherstellen, dass der MIDL-Compiler und der C-Compiler für alle [**char-**](char-idl.md) und kleinen Typen [**ordnungsgemäß zusammenarbeiten.**](small.md)

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>signed**


</dt> <dd>

Gibt an, dass der C-Compiler-Standardtyp für [**char**](char-idl.md) signiert ist. Alle Vorkommen von **char, die** nicht von einer Vorzeichenspezifikation begleitet werden, werden als zeichen ohne Vorzeichen generiert.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>unsigned**


</dt> <dd>

Gibt an, dass der C-Compiler-Standardtyp für [**char**](char-idl.md) nicht signiert ist. Alle Verwendungen von [**"small"**](small.md) werden nicht zusammen mit einer Vorzeichenspezifikation als klein mit Vorzeichen generiert.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7**


</dt> <dd>

Gibt an, dass [**alle char-Werte**](char-idl.md) ohne ein bestimmtes Sign-Schlüsselwort an die generierten Dateien übergeben werden sollen. Alle Verwendungen von [**"small"**](small.md) werden nicht zusammen mit einer Vorzeichenspezifikation als klein **generiert.**

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Definitionsgemäß ist MIDL [**char**](char-idl.md) nicht signiert. "Small" ist in Bezug auf **char** definiert ( \# small char definieren), und MIDL [**small**](small.md) wird signiert.

Der **Schalter /char** weist den MIDL-Compiler [](unsigned.md) an, explizite signierte oder nicht signierte Deklarationen in den generierten Dateien anzugeben, wenn die C-Compiler-Signdeklaration mit dem MIDL-Standard für diesen Typ in Konflikt steht. [](signed.md)

Denken Sie daran, dass der MIDL-Compiler die Stubs als C-Quellcode generiert, den Sie als Teil Ihrer Client- und Serverprogramme kompilieren müssen. Einige Compiler verwenden überall [](char-idl.md) dort, wo **char-Daten** im Quellcode angegeben werden, ein zeichensigniertes Zeichen. Der Stub-Quellcode, den der MIDL-Compiler generiert, behandelt alle **char-Daten** als **char ohne Vorzeichen.** Wenn der MIDL-Compiler  einfach alle char-Daten  in der IDL-Datei als char-Daten in den Stubs generiert, würden Compiler, die ein signiertes **zeichen** für **char-Daten** verwenden, einen Konflikt im Stub-Quellcode verursachen.

Der Befehlszeilenschalter **/char** dient dazu, diese potenziellen Konflikte zu lösen. Alle als char in der IDL-Datei angegebenen Daten [**werden**](char-idl.md) im Stub-Quellcode als **unsigned char** beibehalten. Außerdem werden kleine [**Daten als**](small.md) signiert verwaltet.

In der folgenden Tabelle werden die generierten Typen zusammengefasst.



| midl /char-Option       | Generierter char-Typ | Generierter kleiner Typ |
|-------------------------|---------------------|----------------------|
| **midl /char signed**   | **unsigned char**   | **small**            |
| **midl /char unsigned** | **char**            | **klein signiert**     |
| **midl /char ascii7**   | **char**            | **small**            |



 

Die **Option /char signed** gibt an, dass der C-Compiler char und kleine Typen signiert sind. Um dem MIDL-Standardwert für **char zu** entsprechen, muss der MIDL-Compiler alle Verwendungen von **char,** die nicht von einer Vorzeichenspezifikation begleitet werden, in **unsigned char konvertieren.** Der [**kleine**](small.md) Typ wird nicht geändert, da dieser C-Compiler-Standardwert dem MIDL-Standard für kleine **entspricht.**

Die **Option /char** unsigned gibt an, dass der C-Compiler [**char-Typ**](char-idl.md) unsigned ist. Der MIDL-Compiler konvertiert alle Verwendungen von [**small**](small.md) nicht zusammen mit einer Vorzeichenspezifikation in einen kleinen mit **Vorzeichen.** 

Die Ascii7-Option gibt an, dass char-Typen keine explizite [**Vorzeichenspezifikation hinzugefügt**](char-idl.md) wird. Der Typ [**small**](small.md) wird als kleiner **generiert.**

Um Verwirrung zu vermeiden, sollten Sie nach Möglichkeit explizite Vorzeichenspezifikationen für [**char**](char-idl.md) und kleine Typen in der IDL-Datei verwenden. Beachten Sie, dass die Verwendung explizit signierter **char-Typen** in Ihrer IDL-Datei von DCE IDL nicht unterstützt wird. Daher ist dieses Feature nicht verfügbar, wenn Sie mit dem MIDL-Switch [**/osf kompilieren.**](-osf.md)

Weitere Informationen zu **/char finden** Sie unter [**small**](small.md).

## <a name="examples"></a>Beispiele

**midl /char signed filename.idl**

**midl /char unsigned filename.idl**

**midl /char ascii7 filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**klein**](small.md)
</dt> </dl>

 

 




