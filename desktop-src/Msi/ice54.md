---
description: ICE54 prüft auf Komponenten, die eine Begleit Datei als Schlüssel Pfad verwenden.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865476"
---
# <a name="ice54"></a>ICE54

ICE54 prüft auf Komponenten, die eine Begleit Datei als Schlüssel Pfad verwenden.

Die Schlüssel Pfad Datei einer Komponente darf nicht von einer anderen Datei abgeleitet werden. Dies kann dazu führen, dass einige Dateien nicht installiert werden. Weitere Informationen zu Begleit Dateien finden Sie in der [Dateitabelle](file-table.md) .

## <a name="result"></a>Ergebnis

ICE54 gibt eine Warnung aus, wenn eine Komponente über eine Schlüssel Pfad Datei verfügt, die Ihre Version von einer anderen Datei ableitet.

## <a name="example"></a>Beispiel

ICE54 gibt die folgende Warnung für das gezeigte Beispiel zurück.

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | Attribut | KEYPATH |
|------------|-----------|---------|
| Component1 | 0         | Datei1   |



 

[Dateitabelle](file-table.md) (partiell)



| File  | Version | Sprache |
|-------|---------|----------|
| Datei1 | Datei2   |          |
| Datei2 | 1.0.0.0 | 1033     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



