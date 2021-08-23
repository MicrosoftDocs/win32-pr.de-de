---
title: IMsRdpCameraRedirConfigCollection EncodingQuality-Eigenschaft
description: Gibt die Codierungsqualität (Bitrate) an.
ms.tgt_platform: multiple
keywords:
- EncodingQuality-Remotedesktopdienste
- EncodingQuality-Eigenschaft Remotedesktopdienste , IMsRdpCameraRedirConfigCollection-Schnittstelle
- IMsRdpCameraRedirConfigCollection-Schnittstelle Remotedesktopdienste , EncodingQuality-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 94537773a54ddeb9bceb2483b7f8db6766f7b3f32f9a8a7fe2d9a24659209870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574430"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a>IMsRdpCameraRedirConfigCollection::EncodingQuality (Eigenschaft)

Gibt die Codierungsqualität (Bitrate) an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a>Eigenschaftswert

Einer der folgenden **CameraRedirEncodingQuality-Enum-Werte,** der die Codierungsqualität (Bitrate) angibt.

| Name des Aufzählmitglieds | Wert |
|-----------------|--------|
| encodingQualityLow | 0x0000 |
| encodingQualityMedium | 0x0001 |
| encodingQualityHigh | 0x0002 |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection ist als AE45252B-AAAB-4504-B681-649D6073A37A definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>