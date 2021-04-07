---
title: helpfile-Attribut
description: Das Attribut \ HelpFile \ legt den Namen der Hilfedatei für eine Typbibliothek fest. Alle Typen in einer Bibliothek verwenden dieselbe Hilfedatei.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- HelpFile-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725161"
---
# <a name="helpfile-attribute"></a>helpfile-Attribut

Das **\[ HelpFile \]** -Attribut legt den Namen der Hilfedatei für eine Typbibliothek fest. Alle Typen in einer Bibliothek verwenden dieselbe Hilfedatei.

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige Identifikationsnummer für die [**Bibliothek**](library.md)an.

</dd> <dt>

*filename* 
</dt> <dd>

Gibt den Namen der Datei an, die den Hilfetext enthält.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die der mittlerer l-Compiler auf die [**Bibliothek**](library.md)anwendet.

</dd> <dt>

*Bibliotheks Anweisungen* 
</dt> <dd>

Gibt eine oder mehrere Mittell-Anweisungen an, die die Bibliotheks Schnittstelle definieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **GetDocumentation** -Funktionen in den Schnittstellen **ITypeLib** und **ITypeInfo** , um den Dateinamen abzurufen.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 