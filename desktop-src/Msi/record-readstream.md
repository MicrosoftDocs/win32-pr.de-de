---
description: Die Read Stream-Methode des Datensatz-Objekts liest eine angegebene Anzahl von Bytes aus einem Daten Satz Feld, das Streamdaten enthält.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Record. Read Stream-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370122"
---
# <a name="recordreadstream-method"></a>Record. Read Stream-Methode

Die Read **Stream** -Methode des [**Datensatz**](record-object.md) -Objekts liest eine angegebene Anzahl von Bytes aus einem Daten Satz Feld, das Streamdaten enthält.

## <a name="syntax"></a>Syntax


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flächen* 
</dt> <dd>

Die erforderliche Feldnummer des Werts im Datensatz, 1-basiert.

</dd> <dt>

*length* 
</dt> <dd>

Die erforderliche Anzahl von Bytes, die aus dem Stream gelesen werden sollen.

</dd> <dt>

*format* 
</dt> <dd>

Erforderliche Interpretation und Rückgabe der Daten bytes.



| Parametername                                                                                                                                                                                                                                                                  | Bedeutung                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**msilesstreaminteger**</dt> <dt>0</dt> </dl> | Als lange ganze Zahl muss die Länge zwischen 1 und 4 liegen.<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**msilestreambytes**</dt> <dt>1</dt> </dl>         | Die Daten als **BSTR**– ein Byte pro Zeichen.<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**msilesstreamansi**</dt> <dt>2</dt> </dl>             | Die ANSI-bytes, die in einen Unicode **BSTR** übersetzt werden.<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**msilesstreamdirect**</dt> <dt>3</dt> </dl>     | Die Byte-Paare, die direkt als **BSTR** zurückgegeben werden.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine Zeichenfolge zurück, die die angeforderte Anzahl der aus einem Daten Satz Feld gelesenen Bytes enthält.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Wert eines nicht vorhandenen Felds ist ein leerer Wert. Wenn der Stream weniger Bytes aufweist, die die Anzahl angefordert hat, wird die zurückgegebene Zeichenfolge entsprechend gekürzt.

Ein Beispiel für diese Methode finden Sie unter [Kopieren der ANSI-Datei in ein Datenbankfeld](copy-ansi-file-into-a-database-field.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




