---
description: Die GetConnected-Methode ruft den an diesen Pin angeschlossenen Pin ab.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: CBasePin.GetConnected-Methode (Amfilter.h)
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
ms.openlocfilehash: 8bac5bc971f67c7678d2160cadb452995165638db4bb44d2ed1c89b3ab08f882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526840"
---
# <a name="cbasepingetconnected-method"></a>CBasePin.GetConnected-Methode

Die `GetConnected` -Methode ruft den Anheften ab, der mit diesem Pin verbunden ist.

## <a name="syntax"></a>Syntax


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins zurück.

## <a name="remarks"></a>Hinweise

Wenn der Pin nicht verbunden ist, gibt diese Methode **NULL** zurück. Rufen Sie die [**CBasePin::IsConnected-Methode**](cbasepin-isconnected.md) auf, um zu bestimmen, ob der Pin verbunden ist.

Die -Methode ruft **AddRef** nicht für die **IPin-Schnittstelle** auf, sodass der Aufrufer die Schnittstelle nicht freigeben sollte.

## <a name="examples"></a>Beispiele

Da der Verweiszähler für den zurückgegebenen Zeiger nicht erhöht wird, können Sie Methodenaufrufe miteinander verketten:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Dieses Codierungsmuster ist sehr praktisch. Wie das Beispiel zeigt, müssen Sie jedoch darauf achten, keinen **NULL-Zeiger** zu dereferenzieren, wenn die Verbindung des Pins nicht hergestellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




