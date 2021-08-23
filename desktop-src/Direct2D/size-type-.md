---
title: Size Type Function (D2d1helper.h)
description: Erstellt eine Größenstruktur, die ihre Breite und Höhe mithilfe des angegebenen Datentyps speichert.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Size Type Function Direct2D
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
ms.openlocfilehash: cf2bac3b43cf083d4f2d3588fed41d55380a435cc10c56cdfdb5cae1929d12c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292780"
---
# <a name="sizetype-function"></a><Type>Size-Funktion

Erstellt eine Größenstruktur, die ihre Breite und Höhe mithilfe des angegebenen Datentyps speichert.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | Beschreibung                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| Typ      | Der Datentyp, der zum Speichern der Breite und Höhe der Größe verwendet wird. Mögliche Werte sind FLOAT und UINT32. |



 

## <a name="parameters"></a>Parameter



| Parameter | Beschreibung        |
|-----------|--------------------|
| width     | Die Breite der Größe.  |
| height    | Die Höhe der Größe. |



 

## <a name="return-value"></a>Rückgabewert

Eine Größe, die die angegebene Breite und Höhe enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate für Windows Vista-Desktop-Apps \[ \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server 2008-Desktop-Apps \[ \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Bibliothek<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





