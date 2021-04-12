---
title: IMsRdpCameraRedirConfigCollection Count-Eigenschaft
description: Gibt die Anzahl der imsrdpcameraredirconfig-Objekte in der Auflistung zurück.
ms.tgt_platform: multiple
keywords:
- Count-Eigenschaft Remotedesktopdienste
- Count-Eigenschaft Remotedesktopdienste, imsrdpcameraredirconfigcollection-Schnittstelle
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.Count
- IMsRdpCameraRedirConfigCollection.get_Count
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31927428b709136de87f436ad92cc6a78fa9795a
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480547"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a>Imsrdpcameraredirconfigcollection:: Count-Eigenschaft

Gibt die Anzahl der [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekte in der Auflistung zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekte in der Auflistung.

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