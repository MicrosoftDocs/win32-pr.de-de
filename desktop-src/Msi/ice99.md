---
description: ICE99 überprüft, ob kein in der Verzeichnis Tabelle eingegebener Eigenschaftsname einen Namen dupliziert, der für die öffentliche oder private Verwendung des Windows Installer reserviert ist.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757039"
---
# <a name="ice99"></a>ICE99

ICE99 überprüft, ob kein in der [Verzeichnis](directory-table.md) Tabelle eingegebener Eigenschaftsname einen Namen dupliziert, der für die öffentliche oder private Verwendung des Windows Installer reserviert ist.

## <a name="result"></a>Ergebnis

ICE99 gibt den folgenden Fehler aus.



| ICE99-Fehler                                                                                                      | BESCHREIBUNG                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Der Verzeichnisname: \[ 1 \] ist mit einer der öffentlichen MSI-Eigenschaften identisch und kann zu unvorhersehbaren Nebeneffekten führen. | Der Wert in der Spalte Verzeichnis der [Verzeichnis](directory-table.md) Tabelle dupliziert einen Eigenschaftsnamen, der vom Windows Installer reserviert ist. |



 

## <a name="example"></a>Beispiel

ICE99 meldet den folgenden Fehler für das Beispiel:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Verzeichnis](directory-table.md) (teilweise)



| Verzeichnis        | Über \_ geordnetes Verzeichnis | DefaultDir |
|------------------|-------------------|------------|
| Customaktiondata |                   |            |



 

Um diese Warnung zu beheben, sollten Sie den Namen von "customaktiondata" ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> <dt>

[Verzeichnis Tabelle](directory-table.md)
</dt> <dt>

[Wird in Windows Installer 3,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



