---
description: Die ColumnInfo-Eigenschaft des View-Objekts gibt ein Record-Objekt zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View.ColumnInfo-Eigenschaft
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
ms.openlocfilehash: 08996c3e77212032eac8f65621c7f8ca9ee8489683295c63fb30092995ad41d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012700"
---
# <a name="viewcolumninfo-property"></a>View.ColumnInfo-Eigenschaft

Die **ColumnInfo-Eigenschaft** des [**View-Objekts**](view-object.md) gibt ein [**Record-Objekt**](record-object.md) zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält. Entweder die Spaltennamen oder die Spaltendefinitionen können angefordert werden. Konstanten, die in der Select-Liste angegeben werden, haben keine Namen.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Informationen für jede Spalte.



| Parametername                                                                                                                                                                                                                                                          | Bedeutung                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Gibt die Namen aller nicht konstanten Spalten im Resultset zurück.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Gibt die Typen aller nicht konstanten Spalten im Resultset zurück.<br/> |



 

## <a name="remarks"></a>Hinweise

Die von der **ColumnInfo-Eigenschaft** zurückgegebenen Spaltenbeschreibungen haben das unter [Spaltendefinitionsformat](column-definition-format.md)beschriebene Format. Jede Spalte wird durch eine Zeichenfolge im entsprechenden Datensatzfeld beschrieben. Die Definitionszeichenfolge besteht aus einem einzelnen Buchstaben, der den Datentyp darstellt, gefolgt von der Breite der Spalte (ggf. in Zeichen oder andernfalls Bytes). Eine Breite von 0 (null) kennzeichnet eine unbegrenzte Breite (lange Textfelder und Streams). Ein Großbuchstabe gibt an, dass NULL-Werte in der Spalte zulässig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView ist als 000C109C-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                |



 

 




