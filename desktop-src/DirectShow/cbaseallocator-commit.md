---
description: 'Die Commit-Methode ordnet den Speicher für die Puffer zu. Diese Methode implementiert die imemzuzucator:: Commit-Methode.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Cbasezucator. Commit-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351326"
---
# <a name="cbaseallocatorcommit-method"></a>Cbasezucator. Commit-Methode

Die- `Commit` Methode ordnet den Speicher für die Puffer zu. Diese Methode implementiert die [**imemzuzucator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Liste aufgeführt.



| Rückgabecode                                                                                       | Beschreibung                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                |
| <dl> <dt>**VFW \_ E \_ sizenotset**</dt> </dl> | Die Puffer Anforderungen wurden nicht angegeben.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie vor dem Aufrufen dieser Methode die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode auf, um die Puffer Anforderungen anzugeben.

Diese Methode ruft die virtuelle Methode [**cbaseallocator:: Alloc**](cbaseallocator-alloc.md) auf, um den Speicher für die Puffer zuzuweisen. Abgeleitete Klassen können die **Zuweisung** überschreiben. Wenn ein Decommit-Vorgang aussteht, wird er abgebrochen.

Sie müssen diese Methode aufrufen, bevor Sie die [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




