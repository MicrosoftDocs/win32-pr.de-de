---
title: IMsRdpClipboard CanSyncLocalClipboardToRemoteSession-Methode
description: Gibt an, ob die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann.
ms.tgt_platform: multiple
keywords:
- Cansynclocalclipboardtoremotesession-Methode Remotedesktopdienste
- Cansynclocalclipboardtoremotesession-Methode Remotedesktopdienste, imsrdpclipboard-Schnittstelle
- Imsrdpclipboard Interface Remotedesktopdienste, cansynclocalclipboardtoremotesession-Methode
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106344152"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>Imsrdpclipboard:: cansynclocalclipboardtoremotesession-Methode

Gibt an, ob die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann.

## <a name="syntax"></a>Syntax

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parameter

**True** , wenn die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann. andernfalls **false**.

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ imsrdpclipboard ist als 2e769ee8-00c7-43dc-afd9-235d75b72a40 definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>