---
description: Ruft die Softwareversion für diesen Datenstrom ab.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Cpersiststream. getsoftwareversion-Methode (pStream. h)
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
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370151"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>Cpersiststream. getsoftwareversion-Methode

Ruft die Softwareversion für diesen Datenstrom ab.

## <a name="syntax"></a>Syntax


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD** zurück, das die Versionsnummer enthält. Jedes Mal, wenn das Format des Streams geändert wird, sollte diese Funktion so geändert werden, dass Sie eine größere Zahl als zuvor zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




