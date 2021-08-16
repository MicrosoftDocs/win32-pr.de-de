---
title: IMsRdpClipboard SyncRemoteClipboardToLocalSession-Methode
description: Synchronisiert die Remote-Zwischenablage mit der lokalen Sitzung.
ms.tgt_platform: multiple
keywords:
- SyncRemoteClipboardToLocalSession-Remotedesktopdienste
- SyncRemoteClipboardToLocalSession-Methode Remotedesktopdienste, IMsRdpClipboard-Schnittstelle
- IMsRdpClipboard-Remotedesktopdienste, SyncRemoteClipboardToLocalSession-Methode
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e1e56a67504ab3182ed6ccaba97591e8259d6e46b6ebdd3bdc06fbaf63c170f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000820"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>IMsRdpClipboard::SyncRemoteClipboardToLocalSession-Methode

Synchronisiert die Remote-Zwischenablage mit der lokalen Sitzung.

## <a name="syntax"></a>Syntax

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

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