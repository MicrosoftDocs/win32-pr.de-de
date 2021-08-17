---
description: In \_ der Tabelle Speicher werden eingebettete OLE-Datenspeicher aufgeführt. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer -Anweisung SQL wird.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee16db075df86e5c5a9c794d3320b49052cf746023bd70e02305d6ce079dbbf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146073"
---
# <a name="_storages-table"></a>\_Tabelle "Speicher"

In \_ der Tabelle Speicher werden eingebettete OLE-Datenspeicher aufgeführt. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer -Anweisung SQL wird.



| Spalte | Typ                 | Key | Nullwerte zulässig |
|--------|----------------------|-----|----------|
| Name   | [Text](text.md)     | J   | N        |
| Daten   | [Binär (Binary)](binary.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Ein eindeutiger Schlüssel, der den Speicher identifiziert. Die maximale Länge von Name beträgt 31 Zeichen.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Daten
</dt> <dd>

Die unformatierten Binärdaten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um einer Datenbank einen OLE-Speicher hinzuzufügen, erstellen Sie einen neuen Datensatz in der Tabelle Speicher, und geben Sie den Namen des \_ Speichers in die Spalte Name ein. Verwenden [**Sie MsiRecordSetStream,**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) um Daten in die Datenspalte dieses Datensatzes zu kopieren. Verwenden Sie abschließend [**MsiViewModify,**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) um den Datensatz in die \_ Storages-Tabelle einfügungen.

Daten können nicht aus der \_ Storages-Tabelle gelesen werden. Die Tabelle Speicher kann jedoch abgefragt werden, um das Vorhandensein eines \_ bestimmten Speichers zu überprüfen. Dies bedeutet, dass es nicht möglich ist, einen OLE-Speicher aus einer Datenbank in eine andere zu verschieben. Stattdessen müssen Sie die ursprüngliche Speicherdatei in die neue Datenbank importieren. Rufen Sie zum Löschen eines OLE-Speichers den Datensatz ab, der die Binärdaten enthält, legen Sie die Spalte Daten in der Tabelle Speicher auf NULL fest, und aktualisieren \_ Sie dann den Datensatz. Eine alternative Methode besteht in der einfachen Löschung des Datensatzes mit [**msiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder einer einfachen SQL Abfrage.

Um einen OLE-Speicher umzubenennen, aktualisieren Sie die Spalte Name des Datensatzes.

Wenn eine Zurückhalten-Anweisung für diese Tabelle mithilfe von SQL (ALTER TABLE) <table> HOLD) oder eine Spalte mit HOLD hinzugefügt wird, muss die Tabelle mit FREE freigegeben werden. Speicher werden erst geschrieben, wenn die Tabelle freigegeben oder ein Committed dafür verwendet wurde.

 

 



