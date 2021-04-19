---
description: Ändert das Änderungsflag für den aktuellen Stream.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Cpersiststream. SetDirty-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361532"
---
# <a name="cpersiststreamsetdirty-method"></a>Cpersiststream. SetDirty-Methode

Ändert das Änderungsflag für den aktuellen Stream.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nicht geändert* 
</dt> <dd>

Neues Änderungsflag für diesen Stream. " **True** " bedeutet, dass die Daten nicht gespeichert wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




