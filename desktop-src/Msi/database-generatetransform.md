---
description: Die GenerateTransform-Methode des Database-Objekts erstellt eine Transformation, die bei Anwendung auf die Objektdatenbank die Verweis Datenbank ergibt. Die Transformation wird im Speicher Objekt gespeichert.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database. GenerateTransform-Methode
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
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356418"
---
# <a name="databasegeneratetransform-method"></a>Database. GenerateTransform-Methode

Die **GenerateTransform** -Methode des [**Database**](database-object.md) -Objekts erstellt eine [*Transformation*](t-gly.md) , die bei Anwendung auf die Objektdatenbank die Verweis Datenbank ergibt. Die Transformation wird im Speicher Objekt gespeichert.

Wenn die Transformation während einer Installation angewendet werden soll, müssen Sie den Zusammenfassungs Informationsdaten Strom mithilfe [**der Methode "**](database-createtransformsummaryinfo.md) -Methode" mit der Methode "-Methode" auffüllen.

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

Erforderliche Datenbank, in der die Änderungen nicht enthalten sind.

</dd> <dt>

*storage* 
</dt> <dd>

Der Name der generierten Transformations Datei. Diese Eingabe ist optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Transformation kann am Ende einer Tabelle nicht-Primärschlüssel Spalten hinzufügen. Eine Transformation kann nicht erstellt werden, mit der einer Tabelle Primärschlüssel Spalten hinzugefügt werden. Eine Transformation kann nicht erstellt werden, um die Reihenfolge, die Namen oder die Definitionen von Spalten zu ändern.

Diese Methode gibt einen booleschen Wert zurück. Wenn eine Transformation generiert wird, wird true zurückgegeben. Wenn eine Transformation nicht generiert wird, wird false zurückgegeben, da es keine Unterschiede zwischen den beiden Datenbanken gibt. Wenn die Methode fehlschlägt, wird ein Fehler generiert.

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

 

 




