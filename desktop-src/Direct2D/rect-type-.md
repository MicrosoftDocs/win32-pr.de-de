---
title: Rect-Typfunktion (D2d1helper. h)
description: Erstellt eine Rechteck Struktur, die seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Rect-Typfunktion Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338752"
---
# <a name="recttype-function"></a>Rect- <Type> Funktion

Erstellt eine Rechteck Struktur, die seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | BESCHREIBUNG                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| type      | Der Datentyp, der zum Speichern der Abmessungen des Rechtecks verwendet wird. Mögliche Werte sind **float** und **UInt32**. |



 

## <a name="parameters"></a>Parameter



| Parameter | BESCHREIBUNG                                             |
|-----------|---------------------------------------------------------|
| Linker Join      | Die x-Koordinate der oberen linken Ecke des Rechtecks.  |
| top       | Die y-Koordinate der oberen linken Ecke des Rechtecks.  |
| Rechts     | Die x-Koordinate der unteren rechten Ecke des Rechtecks. |
| bottom    | Die y-Koordinate der unteren rechten Ecke des Rechtecks. |



 

## <a name="return-value"></a>Rückgabewert

Eine Rechteck Struktur, die die angegebenen Koordinaten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Bibliothek<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





