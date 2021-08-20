---
description: Die ApplyTransform-Methode des Database-Objekts wendet die Transformation auf diese Datenbank an.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database.ApplyTransform-Methode
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
ms.openlocfilehash: 9c3424dab82b6981af033b40b33481937fd7c36d3c00dcf3ddfcba5f13f56ec7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289620"
---
# <a name="databaseapplytransform-method"></a>Database.ApplyTransform-Methode

Die **ApplyTransform-Methode** des [**Database-Objekts**](database-object.md) wendet die Transformation auf diese Datenbank an.

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

Pfad zur transformationsdatei, die angewendet wird. Dieser Parameter ist erforderlich.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Gibt die Fehlerbedingungen an, die unterdrückt werden sollen. Geben Sie als Kombination der folgenden ganzzahligen Werte an.



| Fehlerzustand                                                                                                                                                                                                                                                                                                                                                  | Bedeutung                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt> </dl>                                 | Fügt eine Zeile hinzu, die bereits vorhanden ist.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt> </dl>         | Löscht eine Zeile, die nicht vorhanden ist.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt> </dl>                         | Fügt eine Tabelle hinzu, die bereits vorhanden ist.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt> </dl> | Löscht eine Tabelle, die nicht vorhanden ist.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt> </dl>         | Aktualisiert eine Zeile, die nicht vorhanden ist.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt> </dl>                                 | Transformations- und Datenbankcodeseiten stimmen nicht überein und beide haben keine neutrale Codepage.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt> </dl>                                     | Erstellt die temporäre [ \_ TransformView-Tabelle.](-transformview-table.md)<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **ApplyTransform-Methode** verzögert die Transformation von Tabellen bis zum letzten möglichen Zeitpunkt. In **ApplyTransform** werden die Tabellen- und Spaltenkataloge für die Datenbank sofort transformiert. Die Tabellen- und Spaltenkataloge werden entsprechend der hinzugefügten oder gelöschten Tabelle und der hinzugefügten Spalte aktualisiert (das Löschen von Spalten ist nicht zulässig). Wenn eine Tabelle derzeit in den Arbeitsspeicher geladen wird und transformiert werden muss, wird sie transformiert. Andernfalls wird der Tabellenzustand auf festgelegt, der eine Transformation erfordert, sodass beim Laden der Tabelle oder beim Commit der Datenbank die Transformation angewendet wird. Transformieren in dieser Instanz bedeutet, dass die tatsächlichen (Zeilen-)Daten der Tabelle hinzugefügt, gelöscht oder aktualisiert werden.

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Datenbank**](database-object.md)
</dt> <dt>

[Datenbanktransformationen](database-transforms.md)
</dt> </dl>

 

 




