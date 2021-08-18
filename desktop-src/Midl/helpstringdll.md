---
title: helpstringdll-Attribut
description: Das \helpstringdll\-Attribut legt den Namen der DLL fest, die zum Ausführen einer Dokumentzeichenfolgensuche verwendet werden soll.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- helpstringdll-Attribut MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f773ed18e72f184305275ce238ddf0576c81447181a0b7fb420c30341935f5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067250"
---
# <a name="helpstringdll-attribute"></a>helpstringdll-Attribut

Das **\[ \] helpstringdll-Attribut** legt den Namen der DLL fest, die zum Ausführen einer Dokumentzeichenfolgensuche verwendet werden soll.

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

*help-text-string* 
</dt> <dd>

Eine auf null endende Zeichenfolge, die den vollqualifizierten Dateinamen einer DLL angibt.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Andere Attribute, die für die bibliotheks-Anweisung als Ganzes gelten.

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Bezeichner, den Softwarekomponenten verwenden, um diese [**Bibliothek**](library.md)zu kennzeichnen.

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Eine oder mehrere MIDL-Anweisung, die die Schnittstelle der [**Bibliothek**](library.md)definiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie das **\[ \] helpstringdll-Attribut** für eine Bibliotheks-Anweisung, um als Zeichenfolge den vollqualifizierten Dateinamen einer Dynamic Link Library anzugeben. Dadurch kann ein Benutzer eine Beschreibung der DLL mit dem Objekt-Viewer anzeigen.

Verwenden Sie die **GetDocumentation2-Funktionen** in den **Schnittstellen ITypeLib2** und **ITypeInfo2,** um die Hilfezeichenfolge abzurufen.

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

 

 