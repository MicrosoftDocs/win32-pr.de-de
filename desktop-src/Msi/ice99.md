---
description: ICE99 überprüft, ob kein in der Verzeichnistabelle eingegebener Eigenschaftenname einen Namen dupliziert, der für die öffentliche oder private Verwendung des Windows installer reserviert ist.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25744243ad5de8adc6a88ebc09890eb006d94e929a56e469ce802ad67f9a230b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315270"
---
# <a name="ice99"></a>ICE99

ICE99 überprüft, ob kein in [](directory-table.md) der Verzeichnistabelle eingegebener Eigenschaftenname einen Namen dupliziert, der für die öffentliche oder private Verwendung des Windows ist.

## <a name="result"></a>Ergebnis

ICE99 gibt den folgenden Fehler aus.



| ICE99-Fehler                                                                                                      | BESCHREIBUNG                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Der Verzeichnisname 1 ist mit einer der öffentlichen MSI-Eigenschaften identisch \[ \] und kann unvorhergesehene Nebeneffekte verursachen. | Der Wert in der Spalte Verzeichnis der [Directory-Tabelle](directory-table.md) dupliziert einen Eigenschaftennamen, der vom Windows ist. |



 

## <a name="example"></a>Beispiel

ICE99 meldet den folgenden Fehler für das Beispiel:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Verzeichnis](directory-table.md) (partiell)



| Verzeichnis        | Übergeordnetes \_ Verzeichnis | DefaultDir |
|------------------|-------------------|------------|
| Customactiondata |                   |            |



 

Um diese Warnung zu korrigieren, sollten Sie den Namen von CustomActionData ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> <dt>

[Verzeichnistabelle](directory-table.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.0 und früher](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



