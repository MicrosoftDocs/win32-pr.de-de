---
description: Bildfrequenz eines Videomedientyps in Frames pro Sekunde.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: MF_MT_FRAME_RATE Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb49da7667286c17bfa500a8a90a9f7083e786483120e40ba2d635710668a4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113810"
---
# <a name="mf_mt_frame_rate-attribute"></a>MF \_ MT \_ FRAME \_ RATE-Attribut

Bildfrequenz eines Videomedientyps in Frames pro Sekunde.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Die Bildfrequenz wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attributwerts enthalten den Zähler und die unteren 32 Bits den Nenner. Wenn die Bildfrequenz beispielsweise 30 Frames pro Sekunde (fps) beträgt, beträgt das Verhältnis 30/1. Wenn die Bildfrequenz 29,97 fps beträgt, beträgt das Verhältnis 30.000/1001.

Verwenden Sie zum Festlegen des Werts die [**MFSetAttributeRatio-Funktion.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) Verwenden Sie die [**MFGetAttributeRatio-Funktion,**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) um den Wert abzurufen.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Bildfrequenz für einen Videomedientyp festgelegt.


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



Im folgenden Beispiel wird die Bildfrequenz von einem Videomedientyp abgeleitet.


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




