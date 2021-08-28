---
title: IMsRdpCameraRedirConfigCollection BySymbolicLink-Eigenschaft
description: Gibt ein IMsRdpCameraRedirConfig-Objekt aus der Auflistung zurück, das der angegebenen **symbolischen** Verknüpfung der KSCATEGORY_VIDEO_CAMERA-Schnittstelle für die Kamera entspricht.
ms.tgt_platform: multiple
keywords:
- BySymbolicLink-Remotedesktopdienste
- BySymbolicLink-Eigenschaft Remotedesktopdienste , IMsRdpCameraRedirConfigCollection-Schnittstelle
- IMsRdpCameraRedirConfigCollection-Schnittstelle Remotedesktopdienste , BySymbolicLink-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a46cd3daf8cc4270473433bb0c4c20dee0616dba3619b056d33136e0d4dd8f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033630"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>IMsRdpCameraRedirConfigCollection::. BySymbolicLink-Eigenschaft

Gibt ein [IMsRdpCameraRedirConfig-Objekt](imsrdpcameraredirconfig.md) aus der Auflistung zurück, das der angegebenen **symbolischen** Verknüpfung der KSCATEGORY_VIDEO_CAMERA-Schnittstelle für die Kamera entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Eigenschaftswert

Das [IMsRdpCameraRedirConfig-Objekt,](imsrdpcameraredirconfig.md) das der angegebenen symbolischen Verknüpfung entspricht.

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