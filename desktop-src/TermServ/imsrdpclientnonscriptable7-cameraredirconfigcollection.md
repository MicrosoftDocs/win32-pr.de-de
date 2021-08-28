---
title: IMsRdpClientNonScriptable7 CameraRedirConfigCollection-Eigenschaft
description: Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.
ms.tgt_platform: multiple
keywords:
- CameraRedirConfigCollection-Eigenschaft Remotedesktopdienste
- CameraRedirConfigCollection-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable7-Schnittstelle
- IMsRdpClientNonScriptable7-Schnittstelle Remotedesktopdienste , CameraRedirConfigCollection -Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ea90c06403c1ba44e129867f2d739990a37ee178ebe5d0b8f4afd684b17eb09e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033170"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>IMsRdpClientNonScriptable7::CameraRedirConfigCollection (Eigenschaft)

Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Eigenschaftswert

Eine [IMsRdpCameraRedirConfigCollection,](imsrdpcameraredirconfigcollection.md) die die Sammlung von Kameras (und den zugehörigen Konfigurationen) darstellt, die für die Umleitung verfügbar sind.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 ist als 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>