---
description: Die "applytransform"-Methode des Datenbankobjekts wendet die Transformation auf diese Datenbank an.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database. applytransform-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361423"
---
# <a name="databaseapplytransform-method"></a>Database. applytransform-Methode

Die " **applytransform** "-Methode des [**Daten Bank**](database-object.md) Objekts wendet die Transformation auf diese Datenbank an.

## <a name="syntax"></a>Syntax


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*storage* 
</dt> <dd>

Der Pfad zur angewendeten Transformations Datei. Dieser Parameter ist erforderlich.

</dd> <dt>

*errorconditions* 
</dt> <dd>

Gibt die Fehlerbedingungen an, die unterdrückt werden sollen. Geben Sie als eine Kombination der folgenden ganzzahligen Werte an.



| Fehlerzustand                                                                                                                                                                                                                                                                                                                                                  | Bedeutung                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msitransformerroradentxistingrow**</dt> <dt>0x0001</dt> </dl>                                 | Fügt eine Zeile hinzu, die bereits vorhanden ist.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msitransformerrordeletenonexistingrow**</dt> <dt>0x0002</dt> </dl>         | Löscht eine Zeile, die nicht vorhanden ist.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msitransformerroradde xistingtable**</dt> <dt>0x0004</dt> </dl>                         | Fügt eine Tabelle hinzu, die bereits vorhanden ist.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msitransformerrordeletenonexistingtable**</dt> <dt>0x0008</dt> </dl> | Löscht eine Tabelle, die nicht vorhanden ist.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msitransformerrorupdatenonexistingrow**</dt> <dt>0x0010</dt> </dl>         | Aktualisiert eine Zeile, die nicht vorhanden ist.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msitransformerrorchangecodepage**</dt> <dt>0x0020</dt> </dl>                                 | Die Transformations-und Daten Bank Codepages stimmen nicht mit einer neutralen Codepage identisch.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**msitransformerrorviewtransform**</dt> <dt>0x0100</dt> </dl>                                     | Erstellt die temporäre [ \_ transformview-Tabelle](-transformview-table.md).<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **applytransform** -Methode verzögert das Transformieren von Tabellen bis zum letzten möglichen Zeitpunkt. Die in **applytransform** beschriebenen Schritte sind die sofortige Transformation der Tabellen-und Spalten Kataloge für die Datenbank. Die Tabellen-und Spalten Kataloge werden entsprechend der hinzugefügten oder gelöschten Tabelle und der hinzugefügten Spalte aktualisiert (das Löschen von Spalten ist nicht zulässig). Wenn eine Tabelle momentan in den Arbeitsspeicher geladen wird und transformiert werden muss, wird Sie transformiert. Andernfalls wird der Tabellen Status auf festgelegt, der eine Transformation erfordert, sodass beim Laden der Tabelle oder beim commitcommit der Datenbank die Transformation angewendet wird. Die Transformation in dieser Instanz bedeutet, dass die tatsächlichen (Zeilen-) Daten der Tabelle hinzugefügt, gelöscht oder aktualisiert werden.

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verbindung**](database-object.md)
</dt> <dt>

[Daten Bank Transformationen](database-transforms.md)
</dt> </dl>

 

 




