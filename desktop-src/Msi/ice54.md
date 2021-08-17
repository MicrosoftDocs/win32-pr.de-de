---
description: ICE54 sucht nach Komponenten, die eine Begleitdatei als Schlüsselpfad verwenden.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00658bb62b5c29b25f9fb653e216920fc776ba6df0e3fc2f8b47bbdf715040b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946607"
---
# <a name="ice54"></a>ICE54

ICE54 sucht nach Komponenten, die eine Begleitdatei als Schlüsselpfad verwenden.

Die Schlüsselpfaddatei einer Komponente darf ihre Version nicht von einer anderen Datei ableiten. Dies kann dazu führen, dass einige Dateien nicht installiert werden können. Weitere Informationen [zu Begleitdateien](file-table.md) finden Sie in der Tabelle Datei.

## <a name="result"></a>Ergebnis

ICE54 gibt eine Warnung aus, wenn eine Komponente über eine Schlüsselpfaddatei verfügt, die ihre Version von einer anderen Datei ableitung.

## <a name="example"></a>Beispiel

ICE54 gibt die folgende Warnung für das gezeigte Beispiel zurück.

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[Komponententabelle](component-table.md) (partiell)



| Komponente  | attribute | KeyPath |
|------------|-----------|---------|
| Komponente1 | 0         | Datei1   |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | Version | Sprache |
|-------|---------|----------|
| Datei1 | Datei2   |          |
| Datei2 | 1.0.0.0 | 1033     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



