---
description: Das Datensatz-Objekt ist ein Container für die Speicherung und Übertragung einer Variablen Anzahl von Werten.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Datensatz-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360906"
---
# <a name="record-object"></a>Datensatz-Objekt

Das **Datensatz** -Objekt ist ein Container für die Speicherung und Übertragung einer Variablen Anzahl von Werten. Felder im Datensatz sind numerisch indiziert und können Zeichen folgen, ganze Zahlen, Objekte und NULL-Werte enthalten. Felder, die die zugeordnete Daten Satz Größe überschreiten, werden als NULL-Werte behandelt. Feldnummer 0 ist reserviert.

## <a name="members"></a>Member

Das **Datensatz** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Datensatz** -Objekt verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**ClearData**](record-cleardata.md)   | Löscht die Daten in allen Feldern und legt Sie auf NULL fest.<br/>                                      |
| [**Formattext**](record-formattext.md) | Formatiert Felder gemäß der Vorlage in Feld 0.<br/>                                      |
| [**ReadStream**](record-readstream.md) | Liest eine angegebene Anzahl von Bytes aus einem Daten Satz Feld, das Streamdaten enthält.<br/>                |
| [**SetStream**](record-setstream.md)   | Kopiert den Inhalt der angegebenen Datei als Streamdaten in das angegebene Datensatz-Feld.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Datensatz** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp           | BESCHREIBUNG                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**DataSize**](record-datasize.md)<br/>       |                       | Gibt die Größe der Daten für das angegebene Feld zurück.<br/>                             |
| [**FieldCount**](record-fieldcount.md)<br/>   |                       | Gibt die Anzahl der Felder des Datensatzes zurück.<br/>                                        |
| [**IntegerData**](record-integerdata.md)<br/> | Lesen/Schreiben<br/> | Überträgt ganzzahlige 32-Bit-Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes.<br/> |
| [**IsNull**](record-isnull.md)<br/>           |                       | Gibt true zurück, wenn das Feld NULL ist, und false, wenn das Feld Daten enthält.<br/>  |
| [**StringData**](record-stringdata.md)<br/>   | Lesen/Schreiben<br/> | Überträgt Zeichen folgen Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Methode "kreaterecord"**](installer-createrecord.md)
</dt> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




