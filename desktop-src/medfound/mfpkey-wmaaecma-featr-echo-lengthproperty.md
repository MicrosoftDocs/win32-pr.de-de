---
description: Gibt die Dauer des Echos an, die der AEC-Algorithmus (Acoustic Echo Cancellation) in Millisekunden verarbeiten kann.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4b8f22b87622c00c296f194cb7ba618c55b04901ac30ce216d7387e2e04033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242027"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH-Eigenschaft

Gibt die Dauer des Echos an, die der AEC-Algorithmus (Acoustic Echo Cancellation) in Millisekunden verarbeiten kann.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

256

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Der AEC-Algorithmus verwendet einen adaptiven Filter, dessen Länge durch die Dauer des Echos bestimmt wird. Es wird empfohlen, dass Anwendungen einen der folgenden Werte verwenden:

-   128
-   256
-   512
-   1024

Der Standardwert beträgt 256 Millisekunden, was für die meisten Büro- und Heimumgebungen ausreichend ist. Bevor Sie diese Eigenschaft festlegen, müssen Sie die [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE-Eigenschaft](mfpkey-wmaaecma-feature-modeproperty.md) auf VARIANT \_ TRUE festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

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

 

 
