---
title: IMsRdpCameraRedirConfig InstanceId-Eigenschaft
description: Ruft die Instanz-ID der Kamera ab.
ms.tgt_platform: multiple
keywords:
- InstanceId-Remotedesktopdienste
- InstanceId-Eigenschaft Remotedesktopdienste , IMsRdpCameraRedirConfig-Schnittstelle
- IMsRdpCameraRedirConfig-Schnittstelle Remotedesktopdienste , InstanceId-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 621c865f9727cf484430d00609dcfcfac2431a514cf2bade714fdd4d81b0408c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401000"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>IMsRdpCameraRedirConfig::InstanceId (Eigenschaft)

Ruft die Instanz-ID der Kamera ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Eigenschaftswert

Die Instanz-ID der Kamera.

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