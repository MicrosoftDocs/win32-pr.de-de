---
title: helpfile-Attribut
description: Das \helpfile\-Attribut legt den Namen der Hilfedatei für eine Typbibliothek fest. Alle Typen in einer Bibliothek verwenden dieselbe Hilfedatei.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- HELPFILE-Attribut MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1557d96f35913e5e1ed9b784bedfc430e6c4d77b65954583ca6923e4728af9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384020"
---
# <a name="helpfile-attribute"></a>helpfile-Attribut

Das **\[ helpfile-Attribut \]** legt den Namen der Hilfedatei für eine Typbibliothek fest. Alle Typen in einer Bibliothek verwenden dieselbe Hilfedatei.

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

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die [**Bibliothek**](library.md)an.

</dd> <dt>

*filename* 
</dt> <dd>

Gibt den Namen der Datei an, die den Hilfetext enthält.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die der MIDL-Compiler auf die [**Bibliothek**](library.md)anwendet.

</dd> <dt>

*Library-Anweisungen* 
</dt> <dd>

Gibt eine oder mehrere MIDL-Anweisungen an, die die Bibliotheksschnittstelle definieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die **GetDocumentation-Funktionen** in den **Schnittstellen ITypeLib** und **ITypeInfo,** um den Dateinamen abzurufen.

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

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 