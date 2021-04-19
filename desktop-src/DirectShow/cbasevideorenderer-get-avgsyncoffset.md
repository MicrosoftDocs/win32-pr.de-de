---
description: Die get \_ avgsyncoffset-Methode ruft den Durchschnitt der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem Zeitpunkt ab, zu dem das Streaming tatsächlich für alle Frames gerendert wurde.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: CBaseVideoRenderer.get_AvgSyncOffset-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357609"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>Cbasevideorenderer. get \_ avgsyncoffset-Methode

Die `get_AvgSyncOffset` -Methode ruft den Durchschnitt der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem Zeitpunkt ab, zu dem das Streaming tatsächlich für alle Frames gerendert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piavg* 
</dt> <dd>

Zeiger auf den Durchschnitt der Zeit, wie zuvor beschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**iqualprop:: get \_ avgsyncoffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




