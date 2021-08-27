---
title: IMsRdpClientNonScriptable7 Clipboard-Eigenschaft
description: Ruft den Zwischenablagecontroller ab, der zum Synchronisieren der lokalen und Remotezwischenablage verwendet wird, wenn die manuelle Synchronisierung der Zwischenablage aktiviert ist.
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Zwischenablageeigenschaft
- Zwischenablageeigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable7-Schnittstelle
- IMsRdpClientNonScriptable7-Schnittstelle Remotedesktopdienste , Clipboard-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 236666cbef369c4f2353ff524ceb7544e62f50d4a7e4a7ac59f3882057a92f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009640"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>IMsRdpClientNonScriptable7::Clipboard-Eigenschaft

Ruft den Zwischenablagecontroller ab, der zum Synchronisieren der lokalen und Remotezwischenablage verwendet wird, wenn die manuelle Synchronisierung der Zwischenablage aktiviert ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Eigenschaftswert

Eine [IMsRdpClipboard,](imsrdpclipboard.md) die den Zwischenablagecontroller darstellt, der zum Synchronisieren der lokalen und Remotezwischenablage verwendet wird, wenn die manuelle Zwischenablagesynchronisierung aktiviert ist (d. h. der Eigenschaftswert [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) ist auf **True** festgelegt).

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