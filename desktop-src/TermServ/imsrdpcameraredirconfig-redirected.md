---
title: IMsRdpCameraRedirConfig Redirected-Eigenschaft
description: Gibt an, ob die Kamera umgeleitet wird oder nicht.
ms.tgt_platform: multiple
keywords:
- Umgeleitete Eigenschaften Remotedesktopdienste
- Umgeleitete Eigenschaften Remotedesktopdienste, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, umgeleitete Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480555"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a>Imsrdpcameraredirconfig:: umgeleitet-Eigenschaft

Gibt an, ob die Kamera umgeleitet wird oder nicht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der angibt, ob die Kamera umgeleitet wird oder nicht.

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