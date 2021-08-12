---
title: IMsRdpClipboard CanSyncLocalClipboardToRemoteSession-Methode
description: Gibt an, ob die lokale Zwischenablage mit der Remotesitzung synchronisiert werden kann.
ms.tgt_platform: multiple
keywords:
- CanSyncLocalClipboardToRemoteSession-Methode Remotedesktopdienste
- CanSyncLocalClipboardToRemoteSession-Methode Remotedesktopdienste, IMsRdpClipboard-Schnittstelle
- IMsRdpClipboard-Schnittstelle Remotedesktopdienste, CanSyncLocalClipboardToRemoteSession-Methode
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
ms.openlocfilehash: dabc12064ff43a2bb64a562d1aa3050681f46c31dd2698154beb1dafe3cfd85e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606915"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession-Methode

Gibt an, ob die lokale Zwischenablage mit der Remotesitzung synchronisiert werden kann.

## <a name="syntax"></a>Syntax

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parameter

**TRUE,** wenn die lokale Zwischenablage mit der Remotesitzung synchronisiert werden kann; Andernfalls **FALSE**.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard ist als 2E769EE8-00C7-43DC-AFD9-235D75B72A40 definiert.          |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>