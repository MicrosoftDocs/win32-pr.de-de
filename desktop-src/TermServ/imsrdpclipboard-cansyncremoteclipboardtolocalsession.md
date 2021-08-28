---
title: IMsRdpClipboard CanSyncRemoteClipboardToLocalSession-Methode
description: Gibt an, ob die Remoteablage mit der lokalen Sitzung synchronisiert werden kann.
ms.tgt_platform: multiple
keywords:
- CanSyncRemoteClipboardToLocalSession-Remotedesktopdienste
- CanSyncRemoteClipboardToLocalSession-Methode Remotedesktopdienste, IMsRdpClipboard-Schnittstelle
- IMsRdpClipboard-Remotedesktopdienste, CanSyncRemoteClipboardToLocalSession-Methode
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
ms.openlocfilehash: 40a9fc5d6dcdc2e96d9ce916bce0567cccc90adf10fcacc5d797f61ed292c116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000840"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession-Methode

Gibt an, ob die Remoteablage mit der lokalen Sitzung synchronisiert werden kann.

## <a name="syntax"></a>Syntax

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parameter

**TRUE,** wenn die Remote-Zwischenablage mit der lokalen Sitzung synchronisiert werden kann; andernfalls **FALSE**.

## <a name="return-value"></a>Rückgabewert

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard ist als 2E769EE8-00C7-43DC-AFD9-235D75B72A40 definiert.          |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>