---
title: IMsRdpCameraRedirConfigCollection Count-Eigenschaft
description: Gibt die Anzahl der IMsRdpCameraRedirConfig-Objekte in der Auflistung zurück.
ms.tgt_platform: multiple
keywords:
- Count-Remotedesktopdienste
- Count-Remotedesktopdienste , IMsRdpCameraRedirConfigCollection-Schnittstelle
- IMsRdpCameraRedirConfigCollection-Schnittstelle Remotedesktopdienste , Count-Eigenschaft
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
ms.openlocfilehash: 8966bcd47793646b678c70eeaf4a263086fb9ced6eb2c56eb7b3821ac3d0f1df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475970"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a>IMsRdpCameraRedirConfigCollection::Count (Eigenschaft)

Gibt die Anzahl der [IMsRdpCameraRedirConfig-Objekte](imsrdpcameraredirconfig.md) in der Auflistung zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [IMsRdpCameraRedirConfig-Objekte](imsrdpcameraredirconfig.md) in der Auflistung.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection ist als AE45252B-AAAB-4504-B681-649D6073A37A definiert.          |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>