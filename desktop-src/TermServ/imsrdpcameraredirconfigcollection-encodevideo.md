---
title: IMsRdpCameraRedirConfigCollection EncodeVideo-Eigenschaft
description: Gibt an, ob der Videostream H.264-codiert ist.
ms.tgt_platform: multiple
keywords:
- EncodeVideo-Eigenschaft Remotedesktopdienste
- EncodeVideo-Eigenschaft Remotedesktopdienste , IMsRdpCameraRedirConfigCollection-Schnittstelle
- IMsRdpCameraRedirConfigCollection-Schnittstelle Remotedesktopdienste , EncodeVideo-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 9eda6fd63953425001906595b0cd8b594496e0f83974ba9d359ed43a639a4164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475960"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a>IMsRdpCameraRedirConfigCollection::EncodeVideo-Eigenschaft

Gibt an, ob der Videostream H.264-codiert ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a>Eigenschaftswert

Ein -Wert, der angibt, ob der Videostream H.264-codiert ist.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection ist als AE45252B-AAAB-4504-B681-649D6073A37A definiert.          |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>