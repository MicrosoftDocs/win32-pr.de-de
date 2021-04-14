---
description: Die Framerate eines Video Medientyps in Frames pro Sekunde.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: MF_MT_FRAME_RATE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393722"
---
# <a name="mf_mt_frame_rate-attribute"></a>MF- \_ MT- \_ Frame \_ Raten Attribut

Die Framerate eines Video Medientyps in Frames pro Sekunde.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Die Framerate wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner. Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1. Wenn die Framerate 29,97 fps beträgt, ist das Verhältnis 30.000/1001.

Verwenden Sie die [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) -Funktion, um den Wert festzulegen. Um den Wert zu erhalten, verwenden Sie die [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) -Funktion.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Framerate für einen Video Medientyp festgelegt.


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



Im folgenden Beispiel wird die Frame Rate aus einem Video Medientyp abgerufen.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[**Mfaveragetimeperframeumframerate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[**Mfframerateesaveragetimeperframe**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




