---
title: Iwmdrmlicense getanalogvideorestrictionlevels-Methode (wmdrmsdk. h)
description: Die getanalogvideorestrictionlevels-Methode ruft alle analogen Video Einschränkungen ab, die für die aktuelle Lizenz festgelegt sind.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Getanalogvideorestrictionlevels-Methode Windows Media-Format
- Getanalogvideorestrictionlevels-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getanalogvideorestrictionlevels-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355895"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a>Iwmdrmlicense:: getanalogvideorestrictionlevels-Methode

Die **getanalogvideorestrictionlevels** -Methode ruft alle analogen Video Einschränkungen ab, die für die aktuelle Lizenz festgelegt sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rganalogvideorestrictions \[ \]* \[out\]
</dt> <dd>

Empfängt ein Array von [**WMDRM-Strukturen für \_ analoge \_ Video \_ Einschränkungen**](wmdrm-analog-video-restrictions.md) . Legen Sie diesen Wert auf **null** fest, um die Anzahl der Elemente im Array in " *PUP*" zu erhalten.

</dd> <dt>

*pkrestriktionen* \[ in, out\]
</dt> <dd>

Die Anzahl der Elemente im Array von Einschränkungen. Wenn *rganalogvideorestrictions* auf **null** festgelegt ist, wird dieser Wert auf die Anzahl der Elemente festgelegt, die im Array benötigt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen für das Array von Einschränkungen Arbeitsspeicher zuweisen. Um dies zu tun, müssen Sie zuerst die-Methode aufrufen, wobei *rganalogvideorestrictions* auf **null** festgelegt ist, wodurch der Wert bei *pkrestrictions* auf die Anzahl der erforderlichen Elemente festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





