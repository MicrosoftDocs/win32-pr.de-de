---
title: Point2-Typfunktion (D2d1helper. h)
description: Erstellt einen Punkt, der seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2-Typfunktion Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346733"
---
# <a name="point2type-function"></a>Point2- <Type> Funktion

Erstellt einen Punkt, der seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | BESCHREIBUNG                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| type      | Der Datentyp, der verwendet wird, um die x-Koordinate und die y-Koordinate des Punkts zu speichern. Mögliche Werte sind float und UInt32. |



 

## <a name="parameters"></a>Parameter



| Parameter | BESCHREIBUNG                    |
|-----------|--------------------------------|
| x         | Die x-Koordinate des Punkts. |
| Y         | Die y-Koordinate des Punkts. |



 

## <a name="return-value"></a>Rückgabewert

Ein Punkt, der die angegebene x-Koordinate und y-Koordinate enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Bibliothek<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





