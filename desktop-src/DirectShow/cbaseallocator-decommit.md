---
description: Die Decommit-Methode hebt die Zuordnung der Zuweisung auf. Diese Methode implementiert die imemzuzucator::D ecommit-Methode.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Cbasezucator. Decommit-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364976"
---
# <a name="cbaseallocatordecommit-method"></a>Cbasezucator. Decommit-Methode

Die-Methode führt einen Commit für `Decommit` die Zuweisung aus. Diese Methode implementiert die [**imemzuzucator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Nachdem diese Methode aufgerufen wurde, können Aufrufe der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode nicht ausgeführt werden. Wenn Beispiele veröffentlicht werden, werden Sie an die kostenlose Liste zurückgegeben. Wenn das letzte Beispiel zurückgegeben wird, ruft die Zuweisung die [**cbasezucator:: Free**](cbaseallocator-free.md) -Methode auf, die den belegten Arbeitsspeicher freigibt. (In der Basisklasse ist **Free** eine rein virtuelle Methode.)

Außerdem werden von dieser Methode alle Threads freigegeben, die bei **GetBuffer** -Aufrufen blockiert werden. Der Aufruf von **GetBuffer** schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




