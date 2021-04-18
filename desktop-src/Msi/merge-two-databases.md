---
description: Die VBScript-Datei WiMerge.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Mit diesem Beispielskript wird eine Windows Installer Datenbank in einer anderen Datenbank zusammengeführt. Weitere Informationen finden Sie unter Zusammenführungen und Transformationen.
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: Zwei Datenbanken zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0254cbe2bd0785b45d4ced3a16770023e617bc63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366286"
---
# <a name="merge-two-databases"></a>Zwei Datenbanken zusammenführen

Die VBScript-Datei WiMerge.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Mit diesem Beispielskript wird eine Windows Installer Datenbank in einer anderen Datenbank zusammengeführt. Weitere Informationen finden Sie unter Zusammenführungen [und Transformationen](merges-and-transforms.md).

Die [**msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) -Funktion und die [**Merge**](database-merge.md) -Methode des [**Daten Bank**](database-object.md) Objekts können nicht zum Zusammenführen eines Moduls verwendet werden, das im Installationspaket enthalten ist. Sie sollten nicht zum Zusammenführen von [Mergemodulen](merge-modules.md) in einem Windows Installer Paket verwendet werden. Wenn Sie ein Mergemodul in ein Installationspaket einschließen möchten, sollten Autoren von Installationspaketen den Richtlinien folgen, die im Thema [Anwenden von Mergemodulen](applying-merge-modules.md) beschrieben werden.

Das Beispiel veranschaulicht die Verwendung folgender:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**Merge-Methode**](database-merge.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)
-   [**FETCH-Methode**](view-fetch.md)
-   [**Objekt anzeigen**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)

Um dieses Beispiel verwenden zu können, müssen Sie über die CScript.exe oder WScript.exe Version von Windows Script Host verfügen. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ Pfad zur Datei \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiMerge.vbs \[ Pfad zum Daten \] \[ bankpfad zum importierten Daten Bank \] \[ Tabellennamen\]**

Geben Sie den Pfad zur Windows Installer Datenbank an, die den Merge empfängt. Geben Sie den Pfad zu der Datenbank an, die in die erste importiert wird. Sie können einen optionalen Namen für eine Tabelle angeben, in der die Zusammenschluss Fehler enthalten sein sollen. Wenn kein Tabellenname angegeben wird, verwendet das Installationsprogramm den Namen \_ mergeerrors und löscht die Tabelle, nachdem der Inhalt angezeigt wurde.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



