---
title: IMsRdpCameraRedirConfigCollection ByInstanceId-Eigenschaft
description: Gibt ein imsrdpcameraredirconfig-Objekt aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.
ms.tgt_platform: multiple
keywords:
- Byinstanceid-Eigenschaft Remotedesktopdienste
- Byinstanceid-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, byinstanceid (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480526"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>Imsrdpcameraredirconfigcollection:: byinstanceid (Eigenschaft)

Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Eigenschaftswert

Das [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt, das der angegebenen Instanz-ID entspricht.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>