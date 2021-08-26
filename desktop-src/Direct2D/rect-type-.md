---
title: Rect-Typfunktion (D2d1helper.h)
description: Erstellt eine Rechteckstruktur, die ihre Koordinaten mithilfe des angegebenen Datentyps speichert.
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
ms.openlocfilehash: 2e5f56fd9cbcfd576a441d9199e7ec1114cfb9f3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884485"
---
# <a name="rectlttypegt-function"></a>&lt;Rect-Typfunktion &gt;

Erstellt eine Rechteckstruktur, die ihre Koordinaten mithilfe des angegebenen Datentyps speichert.

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



| Parameter | Beschreibung                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| Typ      | Der Datentyp, der zum Speichern der Dimensionen des Rechtecks verwendet wird. Mögliche Werte sind **FLOAT** und **UINT32.** |



 

## <a name="parameters"></a>Parameter



| Parameter | BESCHREIBUNG                                             |
|-----------|---------------------------------------------------------|
| Linker Join      | Die x-Koordinate der oberen linken Ecke des Rechtecks.  |
| top       | Die y-Koordinate der oberen linken Ecke des Rechtecks.  |
| Rechts     | Die x-Koordinate der unteren rechten Ecke des Rechtecks. |
| bottom    | Die y-Koordinate der unteren rechten Ecke des Rechtecks. |



 

## <a name="return-value"></a>Rückgabewert

Eine Rechteckstruktur, die die angegebenen Koordinaten enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate für Windows \[ \| Vista-Desktop-Apps UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server 2008-Desktop-Apps \[ \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Bibliothek<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





