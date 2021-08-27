---
title: IMsRdpCameraRedirConfigCollection ByInstanceId-Eigenschaft
description: Gibt ein IMsRdpCameraRedirConfig-Objekt aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.
ms.tgt_platform: multiple
keywords:
- ByInstanceId-Eigenschaft Remotedesktopdienste
- ByInstanceId-Eigenschaft Remotedesktopdienste , IMsRdpCameraRedirConfigCollection-Schnittstelle
- IMsRdpCameraRedirConfigCollection-Schnittstelle Remotedesktopdienste , ByInstanceId-Eigenschaft
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
ms.openlocfilehash: e621efa61c6e033a9066da30fc6a2a97c76ebec94e9bfe848743f8b031b08d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080070"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>IMsRdpCameraRedirConfigCollection::ByInstanceId-Eigenschaft

Gibt ein [IMsRdpCameraRedirConfig-Objekt](imsrdpcameraredirconfig.md) aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Eigenschaftswert

Das [IMsRdpCameraRedirConfig-Objekt,](imsrdpcameraredirconfig.md) das der angegebenen Instanz-ID entspricht.

## <a name="requirements"></a>Requirements (Anforderungen)

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