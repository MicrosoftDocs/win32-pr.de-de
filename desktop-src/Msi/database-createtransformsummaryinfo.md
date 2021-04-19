---
description: Die Methode "kreatetransformsummaryinfo" des Datenbankobjekts erstellt den Zusammenfassungs Informationsdaten Strom einer vorhandenen Transformations Datei und füllt ihn auf. Diese Methode füllt die Eigenschaften mit den Basis-und Referenz-ProductCode und ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database. kreatetransformsummaryinfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369473"
---
# <a name="databasecreatetransformsummaryinfo-method"></a>Database. kreatetransformsummaryinfo-Methode

Die Methode " **kreatetransformsummaryinfo** " des [**Daten Bank**](database-object.md) Objekts erstellt den Zusammenfassungs Informationsdaten Strom einer vorhandenen Transformations Datei und füllt ihn auf. Diese Methode füllt die Eigenschaften mit den Basis-und Referenz- [**ProductCode**](productcode.md) und [**ProductVersion**](productversion.md).

## <a name="syntax"></a>Syntax


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Referenz* 
</dt> <dd>

Erforderliche Datenbank, in der die Änderungen nicht enthalten sind.

</dd> <dt>

*storage* 
</dt> <dd>

Der Name der generierten Transformations Datei. Diese Eingabe ist optional.

</dd> <dt>

*errorconditions* 
</dt> <dd>

Erforderliche Fehlerbedingungen, die unterdrückt werden sollen, wenn die Transformation angewendet wird. Kombinieren Sie einen oder mehrere der folgenden Fehler Bedingungs Werte.



| Name der Fehlerbedingung                                                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <dt>**msitransformerrornone**</dt> <dt>0</dt> </dl>                                                                         | Keine der folgenden Bedingungen.<br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msitransformerroradde xistingrow**</dt> <dt>1</dt> </dl>                                 | Fügt eine Zeile hinzu, die bereits vorhanden ist.<br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msitransformerrordeletenonexistingrow**</dt> <dt>2</dt> </dl>         | Löscht eine Zeile, die nicht vorhanden ist.<br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msitransformerroradde xistingtable**</dt> <dt>4</dt> </dl>                         | Fügt eine Tabelle hinzu, die bereits vorhanden ist.<br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msitransformerrordeletenonexistingtable**</dt> <dt>8</dt> </dl> | Löscht eine Tabelle, die nicht vorhanden ist.<br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msitransformerrorupdatenonexistingrow**</dt> <dt>16</dt> </dl>        | Aktualisiert eine Zeile, die nicht vorhanden ist.<br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msitransformerrorchangecodepage**</dt> <dt>32</dt> </dl>                                | Transformations-und Daten Bank Codepages stimmen nicht zu, und keine der Codepage ist neutral.<br/> |



 

</dd> <dt>

*validation* 
</dt> <dd>

Erforderlich, wenn die Transformation auf eine Datenbank angewendet wird. zeigt an, welche Eigenschaften überprüft werden sollten, um sicherzustellen, dass diese Transformation auf die Datenbank angewendet werden kann. Die Eigenschaften sind alle im Eigenschaften Satz für den [Zusammenfassungs Informationsstrom](summary-information-stream-property-set.md)enthalten.

Kombinieren Sie einen oder mehrere der folgenden Werte.



| Validierungsflag                                                                                                                                                                                                                                                                                                         | Bedeutung                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <dt>**msitransformvalidationnone**</dt> <dt>0</dt> </dl>                 | Es wurde keine Validierung durchgeführt.<br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <dt>**msitransformvalidationlanguage**</dt> <dt>1</dt> </dl> | Die Standardsprache muss der Basisdatenbank entsprechen.<br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <dt>**msitransformvalidationproduct**</dt> <dt>2</dt> </dl>     | Das Produkt muss der Basisdatenbank entsprechen.<br/>          |



 

Wählen Sie zum Überprüfen der Produktversion zunächst mindestens eines dieser drei Flags aus, um anzugeben, wie viel der Version überprüft werden soll.



| Validierungsflag                                                                                                                                                                                                                                                                                                              | Bedeutung                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <dt>**msitransformvalidationmajorver**</dt> <dt>8</dt> </dl>      | Prüft nur die Hauptversion.<br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <dt>**msitransformvalidationminorver**</dt> <dt>16</dt> </dl>     | Prüft nur die Haupt-und neben Version.<br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <dt>**msitransformvalidationupdatever**</dt> <dt>32</dt> </dl> | Überprüft die Haupt-, neben-und Update Versionen.<br/> |



 

Wählen Sie dann eine der folgenden Optionen aus, um die erforderliche Beziehung zwischen der Produktversion der Datenbank, auf die die Transformation angewendet wird, und der der Basisdatenbank anzugeben.



| Validierungsflag                                                                                                                                                                                                                                                                                                                                   | Bedeutung                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <dt>**msitransformvalidationless**</dt> <dt>64</dt> </dl>                                          | Version < Basisversion angewendet<br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <dt>**msitransformvalidationlessorequal**</dt> <dt>128</dt> </dl>             | Angewendete Version <= Basisversion<br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <dt>**msitransformvalidationequal**</dt> <dt>256</dt> </dl>                                     | Angewendete Version = Basisversion<br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <dt>**msitransformvalidationgreaterorequal**</dt> <dt>512</dt> </dl> | Angewendete Version >= Basisversion<br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <dt>**msitransformvalidationgreater**</dt> <dt>1024</dt> </dl>                            | Version > Basisversion angewendet<br/>  |



 

Legen Sie das folgende Flag fest, um zu überprüfen, ob die Transformation auf ein Paket angewendet wird, das über den entsprechenden [**UpgradeCode**](upgradecode.md)verfügt.



| Validierungsflag                                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <dt>**msitransformvalidationupgradecode**</dt> <dt>2048</dt> </dl> | Überprüft, ob die Transformation der geeignete [**UpgradeCode**](upgradecode.md)ist.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um einen Zusammenfassungs Informationsdaten Strom für eine Transformation zu erstellen, müssen die [**ProductCode**](productcode.md) -Eigenschaft und die [**ProductVersion**](productversion.md) - [Eigenschaft](property-table.md) in den Eigenschaften Tabellen der Basis-und der Verweis Datenbank definiert werden. Wenn msitransformvalidationupgradecode verwendet wird, muss die [**UpgradeCode**](upgradecode.md) -Eigenschaft in beiden Datenbanken definiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Daten Bank Transformationen](database-transforms.md)
</dt> </dl>

 

 




