---
title: Size-Typfunktion (D2d1helper. h)
description: Erstellt eine Größen Struktur, die die Breite und Höhe unter Verwendung des angegebenen Datentyps speichert.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Size-Typfunktion Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476257"
---
# <a name="sizetype-function"></a>Size- <Type> Funktion

Erstellt eine Größen Struktur, die die Breite und Höhe unter Verwendung des angegebenen Datentyps speichert.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | BESCHREIBUNG                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| type      | Der Datentyp, der zum Speichern der Breite und Höhe der Größe verwendet wird. Mögliche Werte sind float und UInt32. |



 

## <a name="parameters"></a>Parameter



| Parameter | BESCHREIBUNG        |
|-----------|--------------------|
| width     | Die Breite der Größe.  |
| height    | Die Höhe der Größe. |



 

## <a name="return-value"></a>Rückgabewert

Eine Größe, die die angegebene Breite und Höhe enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Bibliothek<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





