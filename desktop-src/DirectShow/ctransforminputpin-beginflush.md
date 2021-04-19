---
description: 'Die beginflush-Methode startet einen Löschvorgang. Diese Methode implementiert die IPin:: beginflush-Methode.'
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Ctransforminputpin. beginflush-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356494"
---
# <a name="ctransforminputpinbeginflush-method"></a>Ctransforminputpin. beginflush-Methode

Die- `BeginFlush` Methode startet einen Löschvorgang. Diese Methode implementiert die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                     |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die Ausgabepin ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbaseiniputpin:: beginflush**](cbaseinputpin-beginflush.md) -Methode der PIN auf. Anschließend wird die [**ctransformfilter:: beginflush**](ctransformfilter-beginflush.md) -Methode des Filters aufgerufen, um den Aufruf Downstream zu übermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




