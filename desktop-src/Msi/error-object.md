---
description: Das Error-Objekt gibt die Informationen eines einzelnen Merge-Fehlers zurück.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Error-Objekt (Mergemod. h)
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
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357607"
---
# <a name="error-object"></a>Error-Objekt

Das **Error** -Objekt gibt die Informationen eines einzelnen Merge-Fehlers zurück.

## <a name="members"></a>Member

Das **Error** -Objekt verfügt über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Error** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                | BESCHREIBUNG                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Databasekeys**](error-databasekeys.md)<br/>   | Gibt die Primärschlüssel der Zeile in der Datenbanktabelle zurück, die den Fehler verursacht hat.<br/> |
| [**Databasetable**](error-databasetable.md)<br/> | Gibt den Tabellennamen der Tabelle in der Datenbank zurück, die den Fehler verursacht.<br/>           |
| [**Sprache**](error-language.md)<br/>           | Gibt die Sprache des Fehlers zurück.<br/>                                                |
| [**Modulekeys**](error-modulekeys.md)<br/>       | Gibt die Primärschlüssel der Zeile in der Modul Tabelle zurück, die den Fehler verursacht hat.<br/>   |
| [**Moduletable**](error-moduletable.md)<br/>     | Gibt den Tabellennamen der Tabelle im Modul zurück, das den Fehler verursacht.<br/>             |
| [**ADS**](error-path.md)<br/>                   | Gibt den Pfad zur Datei oder zum Verzeichnis zurück, die den Fehler verursacht hat. Derzeit nicht verwendet.<br/>    |
| [**type**](error-type.md)<br/>                   | Gibt den Typ des Fehlers zurück.<br/>                                                        |



 

## <a name="c"></a>C++

Schnittstelle **imsmerror: IDispatch**

## <a name="interface-id"></a>Schnittstellen-ID



| Konstante           | Wert                                  |
|--------------------|----------------------------------------|
| **IID \_ imsmerror** | {0adda828-2c26-11d2-Ad65-00a0c9af11a6} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




