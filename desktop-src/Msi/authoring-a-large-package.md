---
description: Verwenden Sie diese Richtlinie, um ein Windows Installer-Paket zu erstellen, das mehr als 32767 Dateien enthält.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Erstellen eines großen Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d55f7933fe600bd6c0db0705328f18d7eae2f55e3463e3ea03be8118229eca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996880"
---
# <a name="authoring-a-large-package"></a>Erstellen eines großen Pakets

Verwenden Sie diese Richtlinie, um ein Windows Installer-Paket zu erstellen, das mehr als 32767 Dateien enthält.

Wenn Ihr Windows Installer-Paket mehr als 32767 Dateien enthält, müssen Sie das Schema der Datenbank ändern, um den Grenzwert für die folgenden Spalten zu erhöhen:

-   Die Sequence -Spalte der [Dateitabelle](file-table.md).
-   Die LastSequence-Spalte der [Media-Tabelle.](media-table.md)
-   Die Sequenzspalte der [Patchtabelle](patch-table.md).

Weitere Informationen finden Sie unter [Spaltendefinitionsformat](column-definition-format.md).

**So erhöhen Sie den Grenzwert einer Datenbankspalte**

1.  Exportieren Sie die Tabelle in eine IDT-Datei. Weitere Informationen finden Sie unter [Msidb.exe](msidb-exe.md), [Dateien exportieren](export-files.md)und Importieren und [Exportieren von](importing-and-exporting.md).
2.  Bearbeiten Sie die IDT-Datei, um den Spaltentyp von i2 in i4 oder von I2 in I4 zu ändern.
3.  Exportieren Sie [ \_ die Validation-Tabelle](-validation-table.md) in eine IDT-Datei.
4.  Bearbeiten Sie die IDT-Datei, um die Werte in der Spalte MaxValue der [ \_ Tabelle Validation](-validation-table.md) so zu ändern, dass sie den höheren Spaltenbreiten gerecht werden.
5.  Importieren Sie die IDT-Dateien wieder in die Datenbank.

Beachten Sie, dass Transformationen und Patches nicht zwischen zwei Paketen mit unterschiedlichen Spaltentypen erstellt werden können.

 

 



