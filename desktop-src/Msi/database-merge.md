---
description: Die Merge-Methode des Datenbankobjekts führt die Verweis Datenbank mit der Basisdatenbank zusammen.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge-Methode
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
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354659"
---
# <a name="databasemerge-method"></a>Database. Merge-Methode

Die **Merge** -Methode des [**Daten Bank**](database-object.md) Objekts führt die Verweis Datenbank mit der Basisdatenbank zusammen.

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

Das erforderliche [**Daten Bank**](database-object.md) Objekt, das in der Datenbank zusammengeführt werden soll.

</dd> <dt>

*errortable* 
</dt> <dd>

Ein optionaler Name einer Tabelle, die die Namen der Tabellen mit Mergekonflikten, die Anzahl der in Konflikt stehenden Zeilen in der Tabelle und einen Verweis auf die Tabelle mit dem Mergekonflikt enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) -Funktion und die **Merge** -Methode des [**Daten Bank**](database-object.md) Objekts können nicht zum Zusammenführen eines Moduls verwendet werden, das in einem Installationspaket enthalten ist. Sie sollten nicht zum Zusammenführen von [Mergemodulen](merge-modules.md) in einem Windows Installer Paket verwendet werden. Wenn Sie ein Mergemodul in ein Installationspaket einschließen möchten, sollten Autoren von Installationspaketen den Richtlinien folgen, die im Thema [Anwenden von Mergemodulen](applying-merge-modules.md) beschrieben werden.

Die **Merge** -Methode kopiert keine eingebetteten CAB- [Dateien](cabinet-files.md) oder [eingebetteten Transformationen](embedded-transforms.md) aus der Verweis Datenbank in die Zieldatenbank. Eingebettete Datenströme, die in der [binären Tabelle](binary-table.md) oder in der [Symboltabelle](icon-table.md) aufgeführt sind, werden aus der Verweis Datenbank in die Zieldatenbank kopiert. In die Verweis Datenbank eingebettete Storages werden nicht in die Zieldatenbank kopiert.

Wenn keine Tabelle angegeben wird, gibt die allgemeine Fehlermeldung die Anzahl der Tabellen mit Mergekonflikten an. Eine beliebige Tabelle kann zwar übermittelt werden, aber alle anderen Spalten müssen NULL-Werte zulassen, da der Vorgang zum Aktualisieren der [Fehler Tabelle](error-table.md) fehlschlägt, wenn eine Spalte keine NULL-Werte zulässt. Eine neu erstellte Tabelle kann ebenfalls übermittelt werden, da die **Merge** -Methode automatisch die Spalten erstellt, die Sie verwendet, wenn Mergekonflikte gefunden werden. Zum Darstellen von Mergekonflikten werden zwei Spalten verwendet. Die erste Spalte ist der Tabellenname und die Primärschlüssel Spalte. Die zweite Spalte gibt die Anzahl der Zeilen in der Tabelle an, die Mergefehler aufweisen.

Wenn Tabellen mit demselben Namen in beiden Datenbanken nicht mit der Anzahl der Primärschlüssel, den Spaltentypen, der Spalten Anzahl oder den Spaltennamen übereinstimmen, schlägt die **Merge** -Methode fehl und gibt eine Fehlermeldung an, die angibt, was aufgetreten ist.

Damit die Fehler Tabelle beibehalten wird, muss der Fehlerhandler die Datenbank, zu der die Fehler Tabelle gehört, ein Commit für die Datenbank durchsetzen. Allerdings sollte dieser Commit ausgeführt werden, nachdem die dritte Spalte verwendet wurde, um die Verweise auf Tabellen zu erhalten, in denen Mergekonflikte aufgetreten sind.

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




