---
description: Verwenden Sie diese Richtlinie, um ein Windows Installer-Paket zu erstellen, das mehr als 32767 Dateien enthält.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Erstellen eines großen Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355667"
---
# <a name="authoring-a-large-package"></a>Erstellen eines großen Pakets

Verwenden Sie diese Richtlinie, um ein Windows Installer-Paket zu erstellen, das mehr als 32767 Dateien enthält.

Wenn das Windows Installer Paket mehr als 32767 Dateien enthält, müssen Sie das Schema der Datenbank ändern, um den Grenzwert der folgenden Spalten zu erhöhen:

-   Die Sequenz Spalte der [Dateitabelle](file-table.md).
-   Die LastSequence-Spalte der [Medien Tabelle](media-table.md).
-   Die Sequenz Spalte der [patchtabelle](patch-table.md).

Weitere Informationen finden Sie unter [Column Definition Format](column-definition-format.md).

**So erhöhen Sie die Begrenzung einer Daten Bank Spalte**

1.  Exportieren Sie die Tabelle in eine IDT-Datei. Weitere Informationen finden Sie unter [Msidb.exe](msidb-exe.md), [Exportieren von Dateien](export-files.md)und [importieren und exportieren](importing-and-exporting.md).
2.  Bearbeiten Sie die IDT-Datei, um den Spaltentyp von i2 in I4 oder von i2 in I4 zu ändern.
3.  Exportieren Sie die [ \_ Validierungs](-validation-table.md) Tabelle in eine IDT-Datei.
4.  Bearbeiten Sie die IDT-Datei, um die Werte in der Spalte MaxValue der [ \_ Überprüfungs Tabelle so](-validation-table.md) zu ändern, dass Sie die Erhöhung der Spaltenbreite berücksichtigt.
5.  Importieren Sie die IDT-Dateien zurück in die Datenbank.

Beachten Sie, dass Transformationen und Patches nicht zwischen zwei Paketen mit unterschiedlichen Spaltentypen erstellt werden können.

 

 



