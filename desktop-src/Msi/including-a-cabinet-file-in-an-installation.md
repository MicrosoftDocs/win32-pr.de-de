---
description: In diesem Abschnitt wird beschrieben, wie Sie CAB-Dateien in Installationen einschließen Weitere Informationen finden Sie unter Verwenden von Schränken und komprimierten Quellen.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Einschließen einer CAB-Datei in eine Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098e660de3f7ec7097ab02613d75219ac0a0d624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356677"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Einschließen einer CAB-Datei in eine Installation

In diesem Abschnitt wird beschrieben, wie Sie CAB-Dateien in Installationen einschließen Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).

**So schließen Sie eine CAB-Datei in ein Installationspaket ein**

1.  Verwenden Sie ein CAB-Erstellungs Tool, um die Quelldateien in eine CAB-Datei zu komprimieren. Siehe CAB- [Dateien](cabinet-files.md).
2.  Die CAB-Datei muss sich entweder in einem Datenstream innerhalb der MSI-Datei oder in einer separaten CAB-Datei befinden, die sich im Stammverzeichnis der Quell Struktur befindet, die von der [Verzeichnis Tabelle](directory-table.md)angegeben wird.
3.  Bestimmen Sie, ob die Quelle ein komprimierter Typ oder ein gemischter Typ sein soll, der sowohl nicht komprimierte als auch komprimierte Dateien aufweist. Siehe [komprimierte und nicht komprimierte Quellen](compressed-and-uncompressed-sources.md). Legen Sie abhängig vom Typ des Quell Bilds die komprimierten oder unkomprimierten Flag-Bits der " [**Wort count Summary**](word-count-summary.md) "-Eigenschaft fest.
4.  Fügen Sie der [Dateitabelle](file-table.md) einen Datensatz für jede der Dateien in der CAB-Datei hinzu. Geben Sie einen Datei Schlüssel in die Datei Spalte ein, der exakt mit dem Datei Schlüssel der Datei in der CAB-Datei übereinstimmt. Bei den Datei Schlüsseln wird Groß-/Kleinschreibung beachtet. Die Datei Installations Sequenz in der Dateitabelle und der CAB-Datei müssen ebenfalls identisch sein. Die Datei Sequenz wird durch die Sequenznummer in der Sequence-Spalte angegeben. Gehen Sie folgendermaßen vor, um die Sequenznummer für die erste Datei in der CAB-Datei zu erreichen. Suchen Sie den vorhandenen Datensatz in der [Medien Tabelle](media-table.md) mit dem größten Wert in der DiskId-Spalte. Das LastSequence-Feld dieses Datensatzes gibt die letzte Datei Sequenznummer an, die auf dem Medium verwendet wird. Weisen Sie der Dateitabelle die erste Datei der neuen CAB-Datei eine Sequenznummer zu, die größer ist als die. Weisen Sie allen verbleibenden Dateien Sequenznummern in derselben Reihenfolge wie in der CAB-Datei zu. Eine Beschreibung der restlichen Daten Satz Felder finden Sie unter [File Table](file-table.md).
5.  Fügen Sie der [Medien Tabelle](media-table.md) für den Schrank einen Datensatz hinzu. Geben Sie einen Wert im Feld DiskId dieses neuen Datensatzes an, der größer ist als der größte bereits in der Tabelle vorhandene DiskId-Wert. Fügen Sie den Namen der CAB-Ausgabe in das CAB-Feld ein. Dieser Name muss in [Form eines CAB-](cabinet.md) Datentyps vorliegen. Stellen Sie dem Namen das Nummern Zeichen "" als Präfix voran, \# Wenn die CAB-Datei ein in der MSI-Datei gespeichertes Datenstream ist. Beachten Sie, dass bei einem Datenstrom bei der CAB-Datei die Groß-/Kleinschreibung beachtet wird. Wenn die CAB-Datei eine separate Datei ist, wird bei dem Namen der Datei nicht zwischen Groß-und Kleinschreibung unterschieden.
6.  Bestimmen Sie die größte Datei Sequenznummer in der neuen CAB-Datei, indem Sie die Sequence-Spalte der aktualisierten Dateitabelle überprüfen. Geben Sie einen Wert ein, der größer als der Wert für das LastSequence-Feld des neuen Datensatzes der Medien Tabelle ist. Eine Beschreibung der restlichen Daten Satz Felder finden Sie unter [Media Table](media-table.md).
7.  Sie können die CAB-Datei im Installationspaket speichern, indem Sie entweder ein Tool wie Msidb.exe oder die [Datenbankfunktionen](database-functions.md)des Installers verwenden. In den folgenden vier Schritten wird erläutert, wie Sie die CAB-Dateien mithilfe der-Datenbankfunktionen aus einem Programm hinzufügen.
8.  Um die CAB-Datei aus einem Programm zum Installationspaket hinzuzufügen, öffnen Sie mithilfe von [**msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)eine Ansicht in der [ \_ Streams-Tabelle](-streams-table.md) der Datenbank.
9.  Verwenden Sie [**msirecordsetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) , um die Name-Spalte der \_ Streams-Tabelle auf den Namen festzulegen, der in der CAB-Spalte der [Medien Tabelle](media-table.md)angezeigt wird. Lassen Sie das Nummern Zeichen aus: \# .
10. Verwenden Sie [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , um die Datenspalte der \_ Streams-Tabelle auf die Daten der CAB-Datei festzulegen.
11. Verwenden Sie [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , um den Datensatz in der Streams-Tabelle zu aktualisieren \_ .
12. Verwenden Sie die folgende Befehlszeile, um Msidb.exe zum Hinzufügen der CAB-Datei Mycab.cab zum Installationspaket mit dem Namen Mydatabase.msi zu verwenden: Msidb.exe-d mydatabase.msi-a mycab.cab. In diesem Fall sollte die CAB-Spalte der Medien Tabelle die Zeichenfolge: \#mycab.cab enthalten.

 

 



