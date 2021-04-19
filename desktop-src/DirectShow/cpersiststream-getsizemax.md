---
description: Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, einschließlich der Versionsnummer.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Cpersiststream. GetSizeMax-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359401"
---
# <a name="cpersiststreamgetsizemax-method"></a>Cpersiststream. GetSizeMax-Methode

Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, einschließlich der Versionsnummer.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcbSize* 
</dt> <dd>

Ein Zeiger auf die Größe in Bytes, die zum Speichern dieses Streams benötigt wird, einschließlich der Versionsnummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die **IPersistStream:: GetSizeMax** -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




