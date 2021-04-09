---
description: In der \_ Tabelle Storages werden eingebettete OLE-Datenspeicher aufgelistet. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864548"
---
# <a name="_storages-table"></a>\_Tabelle "Storages"

In der \_ Tabelle Storages werden eingebettete OLE-Datenspeicher aufgelistet. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.



| Spalte | Typ                 | Schlüssel | Nullwerte zulässig |
|--------|----------------------|-----|----------|
| Name   | [Text](text.md)     | J   | N        |
| Daten   | [Binär (Binary)](binary.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Ein eindeutiger Schlüssel, der den Speicher identifiziert. Die maximale Länge des Namens beträgt 31 Zeichen.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats
</dt> <dd>

Die unformatierten Binärdaten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um einer Datenbank einen OLE-Speicher hinzuzufügen, erstellen Sie einen neuen Datensatz in der \_ Tabelle "Storages" und geben den Namen des Speichers in die Spalte "Name" ein. Verwenden Sie [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , um Daten in die Datenspalte dieses Datensatzes zu kopieren. Verwenden Sie abschließend [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , um den Datensatz in die \_ Tabelle "Storages" einzufügen.

Daten können nicht aus der Tabelle "Storages" gelesen werden \_ . Allerdings \_ kann die Storages-Tabelle abgefragt werden, um zu überprüfen, ob ein bestimmter Speicher vorhanden ist. Dies bedeutet, dass es nicht möglich ist, einen OLE-Speicher von einer Datenbank in eine andere zu verschieben. Sie müssen stattdessen die ursprüngliche Speicherdatei in die neue Datenbank importieren. Zum Löschen eines OLE-Speichers rufen Sie den Datensatz ab, der die Binärdaten enthält, legen Sie die Datenspalte in der \_ Tabelle Storages auf NULL fest, und aktualisieren Sie dann den Datensatz. Eine alternative Methode besteht darin, den Datensatz einfach entweder mithilfe von [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder einer einfachen SQL-Abfrage zu löschen.

Um einen OLE-Speicher umzubenennen, aktualisieren Sie die Spalte Name des Datensatzes.

Wenn eine Aufbewahrung in dieser Tabelle mithilfe von SQL (alter Table) platziert wird. <table> Halten) oder eine Spalte mit Hold hinzugefügt wird, muss die Tabelle mit Free freigegeben werden. Storages werden erst geschrieben, wenn die Tabelle freigegeben wurde oder ein Commit ausgeführt wurde.

 

 



