---
description: Das Error-Objekt gibt die Informationen eines einzelnen Mergefehlers zurück.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Error-Objekt (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 237cf88b2830bf210e84d016b52b7fd0b0183c0c0072ac8f654663e2cd3c12dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947031"
---
# <a name="error-object"></a>Error-Objekt

Das **Error-Objekt** gibt die Informationen eines einzelnen Mergefehlers zurück.

## <a name="members"></a>Member

Das **Error-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Error-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                | Beschreibung                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | Gibt die Primärschlüssel der Zeile in der Datenbanktabelle zurück, die den Fehler verursacht hat.<br/> |
| [**DatabaseTable**](error-databasetable.md)<br/> | Gibt den Tabellennamen der Tabelle in der Datenbank zurück, die den Fehler verursacht hat.<br/>           |
| [**Sprache**](error-language.md)<br/>           | Gibt die Sprache des Fehlers zurück.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Gibt die Primärschlüssel der Zeile in der Modultabelle zurück, die den Fehler verursacht hat.<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | Gibt den Tabellennamen der Tabelle im Modul zurück, das den Fehler verursacht hat.<br/>             |
| [**Pfad**](error-path.md)<br/>                   | Gibt den Pfad zur Datei oder zum Verzeichnis zurück, die den Fehler verursacht hat. Derzeit nicht verwendet.<br/>    |
| [**type**](error-type.md)<br/>                   | Gibt den Fehlertyp zurück.<br/>                                                        |



 

## <a name="c"></a>C++

Interface **IMsmError: IDispatch**

## <a name="interface-id"></a>Schnittstellen-ID



| Konstante           | Wert                                  |
|--------------------|----------------------------------------|
| **IID \_ IMsmError** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




