---
title: IMsRdpCameraRedirConfig ParentInstanceId-Eigenschaft
description: Ruft die Instanz-ID der übergeordneten Instanz der Kamera ab.
ms.tgt_platform: multiple
keywords:
- Eigenschaft "parametriinstanceid" Remotedesktopdienste
- Eigenschaften Remotedesktopdienste der Eigenschaft "imsrdpcameraredirconfig"
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, parameteninstanceid (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106342537"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a>Imsrdpcameraredirconfig::P arentinstanceid-Eigenschaft

Ruft die Instanz-ID der übergeordneten Instanz der Kamera ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a>Eigenschaftswert

Die ID der übergeordneten Geräte Instanz der Kamera.

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