---
description: Die CreateTransformSummaryInfo-Methode des Database-Objekts erstellt und füllt den Zusammenfassungsinformationsdatenstrom einer vorhandenen Transformationsdatei auf. Diese Methode füllt die Eigenschaften mit der Basis und dem Verweis ProductCode und ProductVersion auf.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database.CreateTransformSummaryInfo-Methode
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
ms.openlocfilehash: e1daa3e31ccfb49e49842994d6203b58534d86c111cd98652e66079fa47322cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745730"
---
# <a name="databasecreatetransformsummaryinfo-method"></a>Database.CreateTransformSummaryInfo-Methode

Die **CreateTransformSummaryInfo-Methode** des [**Database-Objekts**](database-object.md) erstellt und füllt den Zusammenfassungsinformationsdatenstrom einer vorhandenen Transformationsdatei auf. Diese Methode füllt die Eigenschaften mit der Basis aus und verweist auf [**ProductCode**](productcode.md) und [**ProductVersion.**](productversion.md)

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

Erforderliche Datenbank, die die Änderungen nicht enthält.

</dd> <dt>

*storage* 
</dt> <dd>

Der Name der generierten Transformationsdatei. Diese Eingabe ist optional.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Erforderliche Fehlerbedingungen, die unterdrückt werden sollen, wenn die Transformation angewendet wird. Kombinieren Sie einen oder mehrere der folgenden Fehlerbedingungswerte.



| Name der Fehlerbedingung                                                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <dt>**msiTransformErrorNone**</dt> <dt>0</dt> </dl>                                                                         | Keine der folgenden Bedingungen.<br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt> </dl>                                 | Fügt eine Zeile hinzu, die bereits vorhanden ist.<br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt> </dl>         | Löscht eine Zeile, die nicht vorhanden ist.<br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt> </dl>                         | Fügt eine Tabelle hinzu, die bereits vorhanden ist.<br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt> </dl> | Löscht eine Tabelle, die nicht vorhanden ist.<br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt> </dl>        | Aktualisiert eine Zeile, die nicht vorhanden ist.<br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt> </dl>                                | Transformations- und Datenbankcodeseiten stimmen nicht überein, und keine der Codepages ist neutral.<br/> |



 

</dd> <dt>

*validation* 
</dt> <dd>

Erforderlich, wenn die Transformation auf eine Datenbank angewendet wird. zeigt, welche Eigenschaften überprüft werden müssen, um sicherzustellen, dass diese Transformation auf die Datenbank angewendet werden kann. Die Eigenschaften sind alle im [Stream-Eigenschaftensatz für Zusammenfassungsinformationen enthalten.](summary-information-stream-property-set.md)

Kombinieren Sie einen oder mehrere der folgenden Werte.



| Validierungsflag                                                                                                                                                                                                                                                                                                         | Bedeutung                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <dt>**msiTransformValidationNone**</dt> <dt>0</dt> </dl>                 | Keine Überprüfung durchgeführt.<br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <dt>**msiTransformValidationLanguage**</dt> <dt>1</dt> </dl> | Die Standardsprache muss mit der Basisdatenbank übereinstimmen.<br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <dt>**msiTransformValidationProduct**</dt> <dt>2</dt> </dl>     | Das Produkt muss mit der Basisdatenbank übereinstimmen.<br/>          |



 

Um die Produktversion zu überprüfen, wählen Sie zunächst eines oder mehrere dieser drei Flags aus, um anzugeben, wie viel der Version überprüft werden soll.



| Validierungsflag                                                                                                                                                                                                                                                                                                              | Bedeutung                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt> </dl>      | Überprüft nur die Hauptversion.<br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt> </dl>     | Überprüft nur die Haupt- und Nebenversion.<br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt> </dl> | Überprüft Haupt-, Neben- und Updateversionen.<br/> |



 

Wählen Sie dann eine der folgenden Möglichkeiten aus, um die erforderliche Beziehung zwischen der Produktversion der Datenbank, auf die die Transformation angewendet wird, und der Produktversion der Basisdatenbank anzugeben.



| Validierungsflag                                                                                                                                                                                                                                                                                                                                   | Bedeutung                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <dt>**msiTransformValidationLess**</dt> <dt>64</dt> </dl>                                          | Angewendete Version < Basisversion<br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt> </dl>             | Angewendete Version <= Basisversion<br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <dt>**msiTransformValidationEqual**</dt> <dt>256</dt> </dl>                                     | Angewendete Version = Basisversion<br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt> </dl> | Angewendete Version >= Basisversion<br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <dt>**msiTransformValidationGreater**</dt> <dt>1024</dt> </dl>                            | Angewendete Version > Basisversion<br/>  |



 

Um zu überprüfen, ob die Transformation auf ein Paket mit dem entsprechenden [**UpgradeCode**](upgradecode.md)angewendet wird, legen Sie das folgende Flag fest.



| Validierungsflag                                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt> </dl> | Überprüft, ob die Transformation der entsprechende [**UpgradeCode**](upgradecode.md)ist.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um einen Zusammenfassungsinformationsstream für eine Transformation zu erstellen, müssen die Eigenschaften [**ProductCode**](productcode.md) und [**ProductVersion**](productversion.md) in den [Property-Tabellen](property-table.md) der Basis- und Verweisdatenbanken definiert werden. Wenn msiTransformValidationUpgradeCode verwendet wird, muss die [**UpgradeCode-Eigenschaft**](upgradecode.md) in beiden Datenbanken definiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datenbanktransformationen](database-transforms.md)
</dt> </dl>

 

 




