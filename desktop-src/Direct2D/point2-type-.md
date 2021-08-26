---
title: Point2-Typfunktion (D2d1helper.h)
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
ms.openlocfilehash: e79208c0e68736ae91d623622c13bbeb624ab760
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887195"
---
# <a name="point2lttypegt-function"></a>&lt;Point2-Typfunktion &gt;

Erstellt einen Punkt, der seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | Beschreibung                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| Typ      | Der Datentyp, der zum Speichern der x-Koordinate und der y-Koordinate des Punkts verwendet wird. Mögliche Werte sind FLOAT und UINT32. |



 

## <a name="parameters"></a>Parameter



| Parameter | Beschreibung                    |
|-----------|--------------------------------|
| x         | Die x-Koordinate des Punkts. |
| Y         | Die y-Koordinate des Punkts. |



 

## <a name="return-value"></a>Rückgabewert

Ein Punkt, der die angegebene x-Koordinate und y-Koordinate enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate für Windows \[ \| Vista-Desktop-Apps UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server 2008-Desktop-Apps \[ \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Bibliothek<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





