---
description: In der \_ Tabelle Streams werden eingebettete OLE-Datenströme aufgelistet. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358855"
---
# <a name="_streams-table"></a>\_Streams-Tabelle

In der \_ Tabelle Streams werden eingebettete OLE-Datenströme aufgelistet. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.



| Spalte | Typ                 | Schlüssel | Nullwerte zulässig |
|--------|----------------------|-----|----------|
| Name   | [Text](text.md)     | J   | N        |
| Daten   | [Binär (Binary)](binary.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Ein eindeutiger Schlüssel, der den Datenstrom identifiziert. Die maximale Länge des Namens beträgt 62 Zeichen.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats
</dt> <dd>

Die unformatierten Binärdaten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um einen OLE-Datenstrom (z. b. ein Objekt des [Binary](binary.md) -Datentyps) aus einer Datei in eine Datenbank zu kopieren, erstellen Sie einen Datensatz in der \_ Streams-Tabelle, und geben Sie den Namen des Datenstroms in die Spalte Name dieses Datensatzes ein. Kopieren Sie die Daten aus der Datei mithilfe von [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)in die Datenspalte. Verwenden Sie [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , um den neuen Datensatz in die Tabelle einzufügen.

Um einen in einer Datenbank eingebetteten binären Datenstrom zu lesen, verwenden Sie eine SQL-Abfrage, um den Datensatz zu suchen und abzurufen, der die Binärdaten enthält. Verwenden Sie [**msirecordlesestream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) , um die Binärdaten in einen Puffer zu lesen.

Um einen binären Datenstrom von einer Datenbank in eine andere zu verschieben, exportieren Sie zuerst die Daten in eine Datei. Verwenden Sie eine SQL-Abfrage, um den Datenstrom in der Datei zu suchen, und verwenden Sie [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , um die Daten aus der Datei in die Datenspalte der \_ Tabelle Streams der zweiten Datenbank zu kopieren. Dadurch wird sichergestellt, dass jede Datenbank über eine eigene Kopie der Binärdaten verfügt. Sie können binäre Daten nicht aus einer Datenbank in eine andere verschieben, indem Sie einfach einen Datensatz mit den Daten aus der ersten Datenbank abrufen und in die zweite Datenbank einfügen.

Um einen Datenstrom zu löschen, rufen Sie den Datensatz ab, und legen Sie die Datenspalte vor dem Aktualisieren des Datensatzes auf NULL fest. Eine andere Methode besteht darin, den Datensatz aus der Tabelle zu entfernen und ihn entweder mithilfe von [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder einer einfachen SQL-Abfrage zu löschen. Ein Datenstrom sollte nicht in einen Datensatz abgerufen werden, wenn der Stream aus der Tabelle gelöscht wird.

Zum Umbenennen eines OLE-Datenstroms aktualisieren Sie die Spalte "Name" des Datensatzes.

Wenn eine Aufbewahrung in dieser Tabelle mithilfe von SQL (alter Table) platziert wird. <table> Halten) oder eine Spalte mit Hold hinzugefügt wird, muss die Tabelle mit Free freigegeben werden. Streams werden erst geschrieben, wenn die Tabelle freigegeben oder ein Commit ausgeführt wurde.

 

 



