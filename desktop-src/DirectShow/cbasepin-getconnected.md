---
description: Die getconnected-Methode ruft die mit dieser Pin verbundene Pin ab.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Cbasepin. getconnected-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351350"
---
# <a name="cbasepingetconnected-method"></a>Cbasepin. getconnected-Methode

Die- `GetConnected` Methode ruft die mit dieser Pin verbundene Pin ab.

## <a name="syntax"></a>Syntax


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die PIN nicht verbunden ist, gibt diese Methode **null** zurück. Wenden Sie die [**cbasepin:: IsConnected**](cbasepin-isconnected.md) -Methode an, um zu bestimmen, ob die PIN verbunden ist.

Die-Methode ruft keine **adressf** für die **IPin** -Schnittstelle auf, sodass der Aufrufer die-Schnittstelle nicht freigeben darf.

## <a name="examples"></a>Beispiele

Da der Verweis Zähler auf dem zurückgegebenen Zeiger nicht inkrementiert wird, können Sie Methodenaufrufe verketten:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Dieses Codierungs Muster ist sehr praktisch. wie im Beispiel gezeigt, müssen Sie jedoch darauf achten, einen **null** -Zeiger nicht zu dereferenzieren, wenn die PIN nicht verbunden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




