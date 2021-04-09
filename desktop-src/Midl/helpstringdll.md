---
title: Helpstringdll-Attribut
description: Mit dem Attribut \ Helpstringdll \ wird der Name der DLL festgelegt, die zum Durchführen einer Suche nach Dokument Zeichenfolgen verwendet werden soll.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- Helpstringdll-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948640"
---
# <a name="helpstringdll-attribute"></a>Helpstringdll-Attribut

Mit dem **\[ Helpstringdll \]** -Attribut wird der Name der DLL festgelegt, die zum Ausführen einer Dokument Zeichenfolgen-Suche verwendet werden soll.

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Hilfe-Text Zeichenfolge* 
</dt> <dd>

Eine NULL terminierte Zeichenfolge, die den voll qualifizierten Dateinamen einer DLL angibt.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Andere Attribute, die auf die Library-Anweisung als Ganzes angewendet werden.

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Bezeichner, der von Softwarekomponenten verwendet wird, um diese [**Bibliothek**](library.md)zu kennzeichnen.

</dd> <dt>

*Library-Definition-Anweisungen* 
</dt> <dd>

Eine oder mehrere Mittell-Anweisungen, die die-Schnittstelle der [**Bibliothek**](library.md)definieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **\[ Helpstringdll \]** -Attribut einer Library-Anweisung, um als Zeichenfolge den voll qualifizierten Dateinamen einer Dynamic Link Library anzugeben. Dies ermöglicht es einem Benutzer, eine Beschreibung der DLL mit dem Objekt-Viewer anzuzeigen.

Verwenden Sie die **GetDocumentation2** -Funktionen in den Schnittstellen **ITypeLib2** und **ITypeInfo2** , um die Hilfe Zeichenfolge abzurufen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 