---
description: Die GenerateTransform-Methode des Database-Objekts erstellt eine Transformation, die bei Anwendung auf die Objektdatenbank die Verweisdatenbank ergibt. Die Transformation wird im Speicherobjekt gespeichert.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database.GenerateTransform-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c07e7483a43ea4f69eac473c76747447932fba57e53e22f79fa0663d4babc86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129650"
---
# <a name="databasegeneratetransform-method"></a>Database.GenerateTransform-Methode

Die **GenerateTransform-Methode** des [**Database-Objekts**](database-object.md) erstellt eine [*Transformation,*](t-gly.md) die bei Anwendung auf die Objektdatenbank die Verweisdatenbank ergibt. Die Transformation wird im Speicherobjekt gespeichert.

Wenn die Transformation während einer Installation angewendet werden soll, müssen Sie die [**CreateTransformSummaryInfo-Methode**](database-createtransformsummaryinfo.md) verwenden, um den Zusammenfassungsinformationsdatenstrom aufzufüllen.

## <a name="syntax"></a>Syntax


```JScript
Database.GenerateTransform(
  reference,
  storage
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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Transformation kann Spalten ohne Primärschlüssel am Ende einer Tabelle hinzufügen. Es kann keine Transformation erstellt werden, die einer Tabelle Primärschlüsselspalten hinzufügt. Es kann keine Transformation erstellt werden, die die Reihenfolge, Namen oder Definitionen von Spalten ändert.

Diese Methode gibt einen booleschen Wert zurück. True wird zurückgegeben, wenn eine Transformation generiert wird. False wird zurückgegeben, wenn keine Transformation generiert wird, da es keine Unterschiede zwischen den beiden Datenbanken gibt. Wenn die Methode fehlschlägt, wird ein Fehler generiert.

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

 

 




