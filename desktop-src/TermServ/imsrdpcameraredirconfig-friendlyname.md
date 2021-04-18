---
title: IMsRdpCameraRedirConfig FriendlyName-Eigenschaft
description: Ruft den anzeigen amen der Kamera ab.
ms.tgt_platform: multiple
keywords:
- FriendlyName-Eigenschaft Remotedesktopdienste
- FriendlyName-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, FriendlyName-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.FriendlyName
- IMsRdpCameraRedirConfig.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 2ffded502f64426392e89c2d18831770133e352d
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106341084"
---
# <a name="imsrdpcameraredirconfigfriendlyname-property"></a>Imsrdpcameraredirconfig:: FriendlyName-Eigenschaft

Ruft den anzeigen amen der Kamera ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_FriendlyName(
    [out, retval] BSTR* pFriendlyName
);
```

## <a name="property-value"></a>Eigenschaftswert

Der Anzeige Name der Kamera.

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