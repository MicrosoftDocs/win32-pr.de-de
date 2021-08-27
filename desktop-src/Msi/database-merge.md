---
description: Die Merge-Methode des Database-Objekts führt die Verweisdatenbank mit der Basisdatenbank zusammen.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database.Merge-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4fad74e1647413b66ebc6910e739750699f4e641c961eff59ecaacbf1e7a41f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074990"
---
# <a name="databasemerge-method"></a>Database.Merge-Methode

Die **Merge-Methode** des [**Database-Objekts**](database-object.md) führt die Verweisdatenbank mit der Basisdatenbank zusammen.

## <a name="syntax"></a>Syntax


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Referenz* 
</dt> <dd>

Das erforderliche [**Datenbankobjekt,**](database-object.md) das mit der Datenbank zusammengeführt werden soll.

</dd> <dt>

*errorTable* 
</dt> <dd>

Ein optionaler Name einer Tabelle, die die Namen der Tabellen mit Mergekonflikten, die Anzahl der in Konflikt stehenden Zeilen in der Tabelle und einen Verweis auf die Tabelle mit dem Mergekonflikt enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**MsiDatabaseMerge-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) und die **Merge-Methode** des [**Database-Objekts**](database-object.md) können nicht zum Zusammenführen eines Moduls verwendet werden, das in einem Installationspaket enthalten ist. Sie sollten nicht verwendet werden, um [Mergemodule in](merge-modules.md) einem Windows Installer-Paket zusammenführungen. Um ein Mergemodul in ein Installationspaket ein schließen zu können, sollten Autoren von Installationspaketen die Richtlinien befolgen, die im Thema Applying Merge Modules (Anwenden von [Mergemodulen)](applying-merge-modules.md) beschrieben sind.

Die **Merge-Methode** kopiert keine eingebetteten [Schränkdateien](cabinet-files.md) oder [eingebetteten Transformationen](embedded-transforms.md) aus der Verweisdatenbank in die Zieldatenbank. Eingebettete Datenströme, die in [](icon-table.md) der [Binärtabelle](binary-table.md) oder Symboltabelle aufgeführt sind, werden aus der Verweisdatenbank in die Zieldatenbank kopiert. In die Verweisdatenbank eingebettete Speicher werden nicht in die Zieldatenbank kopiert.

Wenn keine Tabelle angegeben wird, gibt die allgemeine Fehlermeldung die Anzahl der Tabellen an, die Mergekonflikte enthalten. Jede Tabelle kann übergeben werden, aber alle anderen Spalten müssen nullable sein, da der Vorgang zum Aktualisieren der [Fehlertabelle](error-table.md) fehlschlägt, wenn eine Spalte nicht NULL-Werte zugibt. Eine neu erstellte Tabelle kann auch übergeben werden, da die **Merge-Methode** automatisch die Spalten erstellt, die sie verwendet, wenn Mergekonflikte gefunden werden. Zwei Spalten werden verwendet, um Mergekonflikte zu präsentieren. Die erste Spalte ist der Tabellenname und die Primärschlüsselspalte. Die zweite Spalte gibt die Anzahl der Zeilen dieser Tabelle an, die Mergefehler haben.

Wenn Tabellen mit demselben Namen in beiden Datenbanken nicht mit der Anzahl der Primärschlüssel, spaltentypen, der Anzahl von Spalten oder den Spaltennamen übereinstimmen, schlägt die **Merge-Methode** fehl und gibt eine Fehlermeldung mit dem Hinweis zurück, was aufgetreten ist.

Damit die Tabelle Error erhalten bleibt, muss der Fehlerhandler einen Commit für die Datenbank, zu der die Tabelle Error gehört, führen. Dieser Commit sollte jedoch erfolgen, nachdem die dritte Spalte verwendet wurde, um die Verweise auf die Tabellen zu erhalten, in denen Mergekonflikte aufgetreten sind.

Wenn bei der Methode ein Fehler auftritt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IDatabase der IID ist als \_ 000C109D-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                            |



 

 




