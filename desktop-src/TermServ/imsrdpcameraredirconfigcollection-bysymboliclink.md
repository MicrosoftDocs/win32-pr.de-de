---
title: IMsRdpCameraRedirConfigCollection BySymbolicLink-Eigenschaft
description: Gibt ein imsrdpcameraredirconfig-Objekt aus der Auflistung zurück, das der angegebenen symbolischen Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera entspricht.
ms.tgt_platform: multiple
keywords:
- Bysymboliclink-Eigenschaft Remotedesktopdienste
- Bysymboliclink-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, bysymboliclink (Eigenschaft)
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
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106346379"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>Imsrdpcameraredirconfigcollection::. Bysymboliclink (Eigenschaft)

Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen symbolischen Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Eigenschaftswert

Das [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt, das der angegebenen symbolischen Verknüpfung entspricht.

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