---
description: Die checksizes-Methode überprüft zuordnereigenschaften mit dem aktuellen Medientyp.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Cimageexeccator. checksizes-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368616"
---
# <a name="cimageallocatorchecksizes-method"></a>Cimageexeccator. checksizes-Methode

Die- `CheckSizes` Methode überprüft die zuordnereigenschaften mit dem aktuellen Medientyp.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRequest* 
</dt> <dd>

Ein Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die angeforderten zuordnereigenschaften beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                           | Beschreibung                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Die angeforderten Eigenschaften sind mit dem Medientyp kompatibel.<br/>     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>          | Die angeforderten Eigenschaften sind mit dem Medientyp nicht kompatibel.<br/> |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die besitzende PIN ist nicht verbunden.<br/>                                 |



 

## <a name="remarks"></a>Bemerkungen

Wenn die-Methode zurückgibt, wenn der Rückgabewert S \_ OK ist, enthält das **cbbuffer** -Element von *pRequest* die tatsächliche Puffergröße. Diese ist möglicherweise größer als die angeforderte Größe, Sie ist jedoch nie kleiner.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagezuordcator-Klasse**](cimageallocator.md)
</dt> </dl>

 

 




