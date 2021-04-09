---
title: IMsRdpCameraRedirConfig SymbolicLink-Eigenschaft
description: Ruft den symbolischen Link der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera ab.
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste SymbolicLink
- Eigenschaften Remotedesktopdienste SymbolicLink, imsrdpcameraredirconfig-Schnittstelle
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, SymbolicLink-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103859937"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a>Imsrdpcameraredirconfig:: SymbolicLink (Eigenschaft)

Ruft den symbolischen Link der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a>Eigenschaftswert

Die symbolische Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera.

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