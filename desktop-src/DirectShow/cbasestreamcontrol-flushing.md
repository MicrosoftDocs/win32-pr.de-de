---
description: Die-Methode wird von der-Basisklasse benachrichtigt, dass die PIN gestartet oder beendet wurde.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Cbasestreamcontrol. geleert-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362019"
---
# <a name="cbasestreamcontrolflushing-method"></a>Cbasestreamcontrol. geleert-Methode

Die- `Flushing` Methode benachrichtigt die-Basisklasse, dass die PIN gestartet oder beendet wurde.

## <a name="syntax"></a>Syntax


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*binprogress* 
</dt> <dd>

Gibt einen booleschen Wert an, der angibt, ob die PIN geleert wird. Verwenden Sie den Wert **true** , wenn die PIN einen Leerungs Vorgang startet, und **false** , wenn die PIN einen Löschvorgang beendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die PIN muss diese Methode innerhalb der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -und [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methoden aufrufen. Geben Sie **true** in **beginflush** und **false** in **endflush** an.

Diese Methode bewirkt, dass die [**cbasestreamcontrol:: checkstreamstate**](cbasestreamcontrol-checkstreamstate.md) -Methode nicht mehr wartet. Während die PIN geleert wird, gibt **checkstreamstate** immer Stream- \_ verwerfen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




