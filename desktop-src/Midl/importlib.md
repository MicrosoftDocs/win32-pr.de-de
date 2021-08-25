---
title: importlib-Attribut
description: Mit der \importlib\-Direktive werden Typen, die bereits in eine andere Typbibliothek kompiliert wurden, für die zu erstellende Typbibliothek verfügbar.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib-Attribut MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d5c4b19800f92e3080d3fb435ddd20d62e4b6fe76986869a0f4da86deabcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895070"
---
# <a name="importlib-attribute"></a>importlib-Attribut

Die **\[ \] importlib-Direktive** stellt Typen, die bereits in eine andere Typbibliothek kompiliert wurden, für die zu erstellende Typbibliothek zur Verfügung.

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*library-attributes* 
</dt> <dd>

Null oder mehr Attribute, die auf die Bibliothek angewendet werden.

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Bezeichner, den Softwarekomponenten verwenden, um diese Bibliothek [**zu bezeichnen.**](library.md)

</dd> <dt>

*Zu importierende Datei* 
</dt> <dd>

Der Name und Speicherort der importierten Datei zur MIDL-Kompilierzeit.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Alle **\[ \] importlib-Anweisungen** müssen den anderen Typbeschreibungen in der Bibliothek voran stehen. Beachten Sie, dass die importierte Bibliothek sowie die generierte Bibliothek mit der Anwendung verteilt werden müssen, damit sie zur Laufzeit verfügbar ist.

In den meisten Fällen sollten Sie die **\[** [**MIDL-Import-Direktive**](import.md) **\]** verwenden, um auf Definitionen aus einem anderen zu verweisen. IDL-Datei in Ihrer . IDL-Datei. Diese Methode stellt Der Typbibliothek alle Informationen aus der ursprünglichen Datei zur Verfügung, während **\[ importlib \]** nur den Inhalt der Typbibliothek einfing.

> [!Note]  
> Die **\[ \] importlib-Direktive** macht jeden typ, der in der importierten Bibliothek definiert ist, aus der zu kompilierenden Bibliothek zugänglich. Um Mehrdeutigkeiten zu vermeiden, wenn doppelte Verweise vorhanden sind, empfiehlt es sich, jeden solchen Verweis wie folgt mit dem entsprechenden Bibliotheksnamen zu qualifizieren:

 

``` syntax
library_name.type
```

Wenn keine solche Qualifikation vorhanden ist, löst MIDL doppelte Verweisdeutigkeiten wie folgt auf:

-   Ab Version 3.1 verwendet MIDL den ersten gefundenen Verweis.
-   Version 3.0 von MIDL, die erste Version von MIDL, die Typbibliotheken generieren kann, verwendet den letzten gefundenen Verweis.

## <a name="examples"></a>Beispiele

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[**import**](import.md)
</dt> <dt>

[Importieren von System-Headerdateien](importing-system-header-files.md)
</dt> <dt>

[Importieren von Dateien und Typbibliotheken](importing-files-and-type-libraries.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 