---
description: Gibt die Dauer von Echo an, die der AEC-Algorithmus (Akustik Echo Abbruch) in Millisekunden verarbeiten kann.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348855"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>Mfpkey \_ wmaaecma \_ featr- \_ Echo \_ Länge (Eigenschaft)

Gibt die Dauer von Echo an, die der AEC-Algorithmus (Akustik Echo Abbruch) in Millisekunden verarbeiten kann.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

256

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Der AEC-Algorithmus verwendet einen adaptiven Filter, dessen Länge durch die Dauer des Echo bestimmt wird. Es wird empfohlen, dass Anwendungen einen der folgenden Werte verwenden:

-   128
-   256
-   512
-   1024

Der Standardwert beträgt 256 Millisekunden. dieser Wert ist für die meisten Office-und Heim Umgebungen ausreichend. Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
