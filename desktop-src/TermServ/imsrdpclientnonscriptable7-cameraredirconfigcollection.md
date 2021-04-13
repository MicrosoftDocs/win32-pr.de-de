---
title: IMsRdpClientNonScriptable7 CameraRedirConfigCollection-Eigenschaft
description: Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.
ms.tgt_platform: multiple
keywords:
- Cameraredirconfigcollection-Eigenschaft Remotedesktopdienste
- Cameraredirconfigcollection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable7-Schnittstelle
- IMsRdpClientNonScriptable7 Interface Remotedesktopdienste, cameraredirconfigcollection (Eigenschaft)
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
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104341398"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>IMsRdpClientNonScriptable7:: cameraredirconfigcollection (Eigenschaft)

Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Eigenschaftswert

Eine [imsrdpcameraredirconfigcollection](imsrdpcameraredirconfigcollection.md) , die die Sammlung der Kameras (und der zugehörigen Konfigurationen) darstellt, die für die Umleitung verfügbar sind.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 ist als 71b4a60a-fe21-46d8-a39b-8e32ba0c5ecc definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>