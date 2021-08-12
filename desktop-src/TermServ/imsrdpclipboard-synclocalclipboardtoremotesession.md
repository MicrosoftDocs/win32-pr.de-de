---
title: IMsRdpClipboard SyncLocalClipboardToRemoteSession-Methode
description: Synchronisiert die lokale Zwischenablage mit der Remotesitzung.
ms.tgt_platform: multiple
keywords:
- SyncLocalClipboardToRemoteSession-Methode Remotedesktopdienste
- SyncLocalClipboardToRemoteSession-Methode Remotedesktopdienste, IMsRdpClipboard-Schnittstelle
- IMsRdpClipboard-Schnittstelle Remotedesktopdienste, SyncLocalClipboardToRemoteSession-Methode
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 516782dcb86dd02b0d3fd31fee5cc463a64b0e86726c826a855e245f37ba5908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606905"
---
# <a name="imsrdpclipboardsynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard::SyncLocalClipboardToRemoteSession-Methode

Synchronisiert die lokale Zwischenablage mit der Remotesitzung.

## <a name="syntax"></a>Syntax

```C++
HRESULT SyncLocalClipboardToRemoteSession();
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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
