---
description: Die ColumnInfo-Eigenschaft des View-Objekts gibt ein Datensatz-Objekt zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View. ColumnInfo-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364915"
---
# <a name="viewcolumninfo-property"></a>View. ColumnInfo-Eigenschaft

Die **ColumnInfo** -Eigenschaft des [**View**](view-object.md) -Objekts gibt ein [**Datensatz**](record-object.md) -Objekt zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält. Es können entweder die Spaltennamen oder die Spaltendefinitionen angefordert werden. Die in der Auswahlliste angegebenen Konstanten haben keine Namen.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Informationen, die für jede Spalte benötigt werden.



| Parametername                                                                                                                                                                                                                                                          | Bedeutung                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msicolumninfonames**</dt> <dt>0</dt> </dl> | Gibt die Namen aller nicht konstanten Spalten im Resultset zurück.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msicolumninfotypes**</dt> <dt>1</dt> </dl> | Gibt die Typen aller nicht konstanten Spalten im Resultset zurück.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die von der **ColumnInfo** -Eigenschaft zurückgegebenen Spalten Beschreibungen weisen das Format auf, das im [Spalten Definitions Format](column-definition-format.md)beschrieben wird. Jede Spalte wird durch eine Zeichenfolge im entsprechenden Daten Satz Feld beschrieben. Die Definitions Zeichenfolge besteht aus einem einzelnen Buchstaben, der den Datentyp gefolgt von der Breite der Spalte darstellt (in Zeichen, falls zutreffend, oder else Bytes). Eine Breite von 0 (null) gibt eine unbegrenzte Breite an (lange Textfelder und Streams). Ein Großbuchstabe gibt an, dass NULL-Werte in der Spalte zulässig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




