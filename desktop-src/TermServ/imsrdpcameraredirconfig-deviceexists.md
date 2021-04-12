---
title: IMsRdpCameraRedirConfig DeviceExists-Eigenschaft
description: Gibt an, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).
ms.tgt_platform: multiple
keywords:
- Deviceist-Eigenschaft Remotedesktopdienste
- Deviceexistiert-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, deviceist-Eigenschaft
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
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480563"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>Imsrdpcameraredirconfig::D eviceist-Eigenschaft

Gibt an, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>Eigenschaftswert

Ein Wert, der angibt, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.            |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>