---
title: IMsRdpCameraRedirConfigCollection ByIndex-Eigenschaft
description: Gibt ein IMsRdpCameraRedirConfig-Objekt nach seinem Index in der Auflistung zurück.
ms.tgt_platform: multiple
keywords:
- ByIndex-Remotedesktopdienste
- ByIndex-Remotedesktopdienste , IMsRdpCameraRedirConfigCollection-Schnittstelle
- IMsRdpCameraRedirConfigCollection-Schnittstelle Remotedesktopdienste , ByIndex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 375c0b110975c6ca791bbbe1f61a5b597b00316242484cd68ef018b7ef4ea88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138963"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a>IMsRdpCameraRedirConfigCollection::ByIndex (Eigenschaft)

Gibt ein [IMsRdpCameraRedirConfig-Objekt](imsrdpcameraredirconfig.md) nach seinem Index in der Auflistung zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Eigenschaftswert

Das [IMsRdpCameraRedirConfig-Objekt,](imsrdpcameraredirconfig.md) das dem angegebenen Index entspricht.

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