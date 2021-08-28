---
description: Ruft die Softwareversion für diesen Stream ab.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: CPersistStream.GetSoftwareVersion-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0ba5e9f3fd3dc5e8f021e40c9cb70d95a136ae7c09d6f43826e436a32854170
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084270"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>CPersistStream.GetSoftwareVersion-Methode

Ruft die Softwareversion für diesen Stream ab.

## <a name="syntax"></a>Syntax


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD zurück,** das die Versionsnummer enthält. Jedes Mal, wenn das Format des Streams geändert wird, sollte diese Funktion so geändert werden, dass sie eine größere Zahl als zuvor zurück gibt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




