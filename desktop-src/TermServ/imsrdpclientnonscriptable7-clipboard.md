---
title: IMsRdpClientNonScriptable7 Clipboard-Eigenschaft
description: Ruft den Zwischenablage Controller ab, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste der Zwischenablage
- Eigenschaften Remotedesktopdienste der Zwischenablage, IMsRdpClientNonScriptable7-Schnittstelle
- IMsRdpClientNonScriptable7 Interface-Remotedesktopdienste, Clipboard-Eigenschaft
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
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103957689"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>IMsRdpClientNonScriptable7:: Clipboard (Eigenschaft)

Ruft den Zwischenablage Controller ab, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Eigenschaftswert

Eine [imsrdpclipboard](imsrdpclipboard.md) , die den Zwischenablage Controller darstellt, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert ist (d. h., der [manualclipboardsyncenabled](imsrdpextendedsettings-property.md) -Eigenschafts Wert ist auf **true** festgelegt

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