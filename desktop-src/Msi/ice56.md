---
description: ICE56 überprüft, ob die Verzeichnisstruktur der MSI-Datei ein einzelnes Stammverzeichnis, das Stammverzeichnis der TARGETDIR-Eigenschaft und der SourceDir-Eigenschafts Wert in der DefaultDir-Spalte der Verzeichnis Tabelle ist.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366078"
---
# <a name="ice56"></a>ICE56

ICE56 überprüft, ob die Verzeichnisstruktur der MSI-Datei ein einzelnes Stammverzeichnis, das Stammverzeichnis der [**TARGETDIR**](targetdir.md) -Eigenschaft und der [**SourceDir**](sourcedir.md) -Eigenschafts Wert in der DefaultDir-Spalte der [Verzeichnis Tabelle](directory-table.md)ist.

Wenn eine MSI-Datei mehrere Stämme aufweist oder einen anderen Stamm als [**TARGETDIR**](targetdir.md)angibt, wird bei einer [administrativen Installation](administrative-installation.md) kein korrektes administratives Abbild erstellt.

Beachten Sie, dass leere Verzeichnisse von ICE56 nicht geprüft werden. Die Verzeichnisstruktur übergibt die Validierung mit mehreren Stamm Verzeichnissen, wenn die zusätzlichen Verzeichnisse leer sind.

## <a name="result"></a>Ergebnis

ICE56 gibt einen Fehler aus, wenn die MSI-Dateien nicht über einen einzelnen Stamm ( [**TARGETDIR**](targetdir.md)) verfügt, oder wenn [**SourceDir**](sourcedir.md) nicht in der DefaultDir-Spalte der [Verzeichnis Tabelle](directory-table.md)angegeben ist.

## <a name="example"></a>Beispiel

ICE56 meldet die folgenden Fehler für das gezeigte Beispiel.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis | Über \_ geordnetes Verzeichnis | DefaultDir |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| Root2     | Root2             | SourceDir  |



 

Um den ersten Fehler zu beheben, sollte der [**TARGETDIR**](targetdir.md) -Stamm einen DefaultDir-Wert von [**SourceDir**](sourcedir.md)aufweisen. SourceDir wird ebenfalls akzeptiert. Möglicherweise ist es möglich, **TARGETDIR** das übergeordnete Element des zweiten Stamms zu machen und den Wert "." in der Spalte "DefaultDir" zu verwenden. Weitere Informationen finden Sie in der [Verzeichnis Tabelle](directory-table.md) .

Um den zweiten Fehler zu beheben, sollte die Verzeichnisstruktur nur einen Stamm namens [**TARGETDIR**](targetdir.md)aufweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



