---
description: In \_ Streams Tabelle werden eingebettete OLE-Datenströme aufgeführt. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer -Anweisung SQL wird.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f3796a3abb402027dc9985991a6ba673f5381d8f35657e7d80b0714c40f1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013338"
---
# <a name="_streams-table"></a>\_Streams Tabelle

In \_ Streams Tabelle werden eingebettete OLE-Datenströme aufgeführt. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer -Anweisung SQL wird.



| Spalte | Typ                 | Key | Nullwerte zulässig |
|--------|----------------------|-----|----------|
| Name   | [Text](text.md)     | J   | N        |
| Daten   | [Binär (Binary)](binary.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Ein eindeutiger Schlüssel, der den Stream identifiziert. Die maximale Länge von Name beträgt 62 Zeichen.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Daten
</dt> <dd>

Die unformatierten Binärdaten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um einen OLE-Datenstrom (z. B. ein Objekt des Datentyps [Binary)](binary.md) aus einer Datei in eine Datenbank zu kopieren, erstellen Sie einen Datensatz in der Streams-Tabelle, geben den Namen des Datenstroms in die Spalte Name dieses Datensatzes ein, und kopieren Sie die Daten aus der Datei mit \_ [**msiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)in die Spalte Daten. Verwenden [**Sie MsiViewModify,**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) um den neuen Datensatz in die Tabelle einfügungen.

Verwenden Sie zum Lesen eines in eine Datenbank eingebetteten binären Datenstroms eine SQL Abfrage, um den Datensatz mit den Binärdaten zu suchen und zu abrufen. Verwenden [**Sie MsiRecordReadStream,**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) um die Binärdaten in einen Puffer zu lesen.

Um einen binären Datenstrom von einer Datenbank in eine andere zu verschieben, exportieren Sie die Daten zunächst in eine Datei. Verwenden Sie eine SQL-Abfrage, um den Datenstrom in der Datei zu suchen, und verwenden Sie [**MsiRecordSetStream,**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) um die Daten aus der Datei in die Datenspalte der Streams-Tabelle der zweiten Datenbank \_ zu kopieren. Dadurch wird sichergestellt, dass jede Datenbank über eine eigene Kopie der Binärdaten verfügt. Sie können binäre Daten nicht einfach aus einer Datenbank in eine andere verschieben, indem Sie einfach einen Datensatz mit den Daten aus der ersten Datenbank abrufen und in die zweite Datenbank einfügen.

Rufen Sie zum Löschen eines Datenstroms den Datensatz ab, und legen Sie die Datenspalte auf NULL fest, bevor Sie den Datensatz aktualisieren. Eine andere Methode besteht im Entfernen des Datensatzes aus der Tabelle, indem Sie ihn entweder mit [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder einer einfachen SQL löschen. Ein Stream sollte nicht in einen Datensatz abgerufen werden, wenn der Stream aus der Tabelle gelöscht wird.

Um einen OLE-Datenstrom umzubenennen, aktualisieren Sie die Spalte "Name" des Datensatzes.

Wenn eine Zurückhalten-Anweisung für diese Tabelle mithilfe von SQL (ALTER TABLE) <table> HOLD) oder eine Spalte mit HOLD hinzugefügt wird, muss die Tabelle mit FREE freigegeben werden. Streams werden erst geschrieben, wenn die Tabelle freigegeben oder ein Committed für die Tabelle geschrieben wurde.

 

 



