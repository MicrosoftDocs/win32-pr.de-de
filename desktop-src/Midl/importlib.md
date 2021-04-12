---
title: importlib-Attribut
description: Die "\ importlib \"-Direktive macht Typen, die bereits in einer anderen Typbibliothek kompiliert wurden, für die zu erstellende Typbibliothek verfügbar.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib-Attribut-Mittel l
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472765"
---
# <a name="importlib-attribute"></a>importlib-Attribut

Die **\[ importlib \]** -Direktive macht Typen, die bereits in einer anderen Typbibliothek kompiliert wurden, für die zu erstellende Typbibliothek verfügbar.

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

*Bibliothek-Attribute* 
</dt> <dd>

0 (null) oder mehr Attribute, die auf die Bibliothek angewendet werden.

</dd> <dt>

*Bibliotheksname* 
</dt> <dd>

Der Bezeichner, der von Softwarekomponenten verwendet wird, um diese [**Bibliothek**](library.md)zu kennzeichnen.

</dd> <dt>

*zu importierende Datei* 
</dt> <dd>

Der Name und Speicherort der importierten Datei zur mittleren Kompilierzeit.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle **\[ importlib \]** -Direktiven müssen den anderen Typbeschreibungen in der Bibliothek vorangestellt sein. Beachten Sie, dass sowohl die importierte Bibliothek als auch die generierte Bibliothek mit der Anwendung verteilt werden müssen, damit Sie zur Laufzeit verfügbar ist.

In den meisten Fällen sollten Sie die **\[** [](import.md) **\]** Direktive Import Direktive verwenden, um auf Definitionen von einem anderen zu verweisen. IDL-Datei in Ihrem. IDL-Datei. Diese Methode stellt die Typbibliothek mit allen Informationen aus der ursprünglichen Datei bereit, während **\[ importlib \]** nur den Inhalt der Typbibliothek enthält.

> [!Note]  
> Die **\[ importlib \]** -Direktive macht den in der importierten Bibliothek definierten Typ innerhalb der zu kompilierende Bibliothek zugänglich. Um Mehrdeutigkeit zu vermeiden, wenn doppelte Verweise vorhanden sind, wird empfohlen, dass Sie jeden Verweis mit dem entsprechenden Bibliotheksnamen wie folgt qualifizieren:

 

``` syntax
library_name.type
```

Wenn diese Qualifizierung nicht vorhanden ist, löst die Mittel l die doppelte Verweis Mehrdeutigkeit wie folgt auf:

-   Ab Version 3,1 verwendet die Mittel l den ersten gefundenen Verweis.
-   In Version 3,0 von "Mittel l", der ersten Version von "Mittel l", die Typbibliotheken generieren konnte, wird der letzte gefundene Verweis verwendet.

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

[**Importieren**](import.md)
</dt> <dt>

[Importieren von System-Headerdateien](importing-system-header-files.md)
</dt> <dt>

[Importieren von Dateien und Typbibliotheken](importing-files-and-type-libraries.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 