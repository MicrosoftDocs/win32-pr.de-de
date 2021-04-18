---
title: IMsRdpClipboard CanSyncRemoteClipboardToLocalSession-Methode
description: Gibt an, ob die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann.
ms.tgt_platform: multiple
keywords:
- Cansynkremoteclipboardtolocalsession-Methode Remotedesktopdienste
- Cansynkremoteclipboardtolocalsession-Methode Remotedesktopdienste, imsrdpclipboard-Schnittstelle
- Imsrdpclipboard Interface Remotedesktopdienste, cansynkremoteclipboardtolocalsession-Methode
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106344153"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>Imsrdpclipboard:: cansynkremoteclipboardtolocalsession-Methode

Gibt an, ob die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann.

## <a name="syntax"></a>Syntax

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parameter

**True** , wenn die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann. andernfalls **false**.

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