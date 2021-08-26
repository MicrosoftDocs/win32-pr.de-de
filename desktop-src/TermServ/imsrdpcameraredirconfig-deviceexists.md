---
title: IMsRdpCameraRedirConfig DeviceExists-Eigenschaft
description: Gibt an, ob das Kameragerät derzeit vorhanden ist (d. h., die Kamera ist verbunden).
ms.tgt_platform: multiple
keywords:
- DeviceExists-Remotedesktopdienste
- DeviceExists-Eigenschaft Remotedesktopdienste , IMsRdpCameraRedirConfig-Schnittstelle
- IMsRdpCameraRedirConfig-Schnittstelle Remotedesktopdienste , DeviceExists-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 617c91491d88736ca60218d71f9dd5aa02ad0f9faeefdda6b872ba9262cec587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990660"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>IMsRdpCameraRedirConfig::D eviceExists(Eigenschaft)

Gibt an, ob das Kameragerät derzeit vorhanden ist (d. h., die Kamera ist verbunden).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>Eigenschaftswert

Ein -Wert, der angibt, ob das Kameragerät derzeit vorhanden ist (d. h., die Kamera ist verbunden).

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig ist als 09750604-D625-47C1-9FCD-F09F735705D7 definiert.            |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>