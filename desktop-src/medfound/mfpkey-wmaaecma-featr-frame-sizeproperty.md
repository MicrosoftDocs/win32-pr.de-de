---
description: Gibt die Audioframegröße an, die vom Spracherfassungs-DSP verwendet wird.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812a9c7b85a36b730caffe7679cc742a3bc029546a12839afd95a8c8ab58bfeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973289"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ FRAME \_ SIZE-Eigenschaft

Gibt die Audioframegröße an, die vom Spracherfassungs-DSP verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Der AEC-Algorithmus (Acoustic Echo Cancellation) verarbeitet PCM-Audiobeispiele nacheinander. Der Wert dieser Eigenschaft ist die Größe des Audioframes in Beispielen. Bevor Sie diese Eigenschaft festlegen, müssen Sie die [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE-Eigenschaft](mfpkey-wmaaecma-feature-modeproperty.md) auf VARIANT \_ TRUE festlegen.

Der Spracherfassungs-DSP unterstützt die folgenden Framegrößen:

-   80
-   128
-   160
-   240
-   256
-   320

Wenn der Wert dieser Eigenschaft 0 (null) ist, wählt der DSP die Framegröße basierend auf dem Systemmodus und dem Ausgabeformat aus.

Um die beste Leistung zu erzielen, wird jedoch empfohlen, dass Anwendungen den Standardwert verwenden. Wenn der Verarbeitungsmodus nur ein Mikrofonarray ist, beträgt der Standardwert 320 Stichproben. Für alle anderen Verarbeitungsmodi ist der Standardwert 160 Stichproben. Weitere Informationen zu den Verarbeitungsmodi des Spracherfassungs-DSP finden Sie unter [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE](mfpkey-wmaaecma-system-modeproperty.md).

Nach dem ersten Aufruf von [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) oder [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)können Sie diese Eigenschaft lesen, um die tatsächliche Framegröße abzurufen, auch wenn [**MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE**](mfpkey-wmaaecma-feature-modeproperty.md) false ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Spracherfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
