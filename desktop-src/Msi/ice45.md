---
description: ICE45 überprüft, ob die Bitfeld Spalten in der Datenbank reservierte Bits nicht auf 1 festlegen.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215703"
---
# <a name="ice45"></a>ICE45

ICE45 überprüft, ob die Bitfeld Spalten in der Datenbank reservierte Bits nicht auf 1 festlegen.

Reservierte Bits bieten keine Funktionalität in den aktuellen Versionen des Installers, aber in zukünftigen Versionen. Sie sollten auf 0 festgelegt werden, um mit zukünftigen Versionen von Windows Installer kompatibel zu sein.

## <a name="result"></a>Ergebnis

ICE45 gibt eine Fehlermeldung aus, wenn eine der folgenden Tabellen ein Bitfeld mit einem reservierten Bit enthält, das auf den Wert 1 festgelegt ist.

-   [Bbcontrol-Tabelle](bbcontrol-table.md)
-   [Dialog Feld Tabelle](dialog-table.md)
-   [Funktions Tabelle](feature-table.md)
-   [Dateitabelle](file-table.md)
-   ["Muvefile"-Tabelle](movefile-table.md)
-   [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)
-   [ODBCDatasource-Tabelle](odbcdatasource-table.md)
-   [Patchtabelle](patch-table.md)
-   [RemoveFile-Tabelle](removefile-table.md)
-   [ServiceControl-Tabelle](servicecontrol-table.md)
-   [Servicabstall-Tabelle](serviceinstall-table.md)
-   [TextStyle-Tabelle](textstyle-table.md)

ICE45 sendet eine von zwei Warnmeldungen, wenn die [Steuerelement Tabelle](control-table.md) ein Bitfeld mit einem reservierten Bit enthält, das auf den Wert 1 festgelegt ist.

## <a name="example"></a>Beispiel

ICE45 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

ICE45 meldet die folgende Warnung für das gezeigte Beispiel.

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

[Dateitabelle](file-table.md) (partiell)



| File  | Attribute |
|-------|------------|
| Datei1 | 128        |



 

[Control-Tabelle](control-table.md) (partiell)



| Dialog  | Control | Attribute |
|---------|---------|------------|
| Dialog1 | Edit1   | 2097152    |
| Dialog1 | Edit2   | 1048576    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



