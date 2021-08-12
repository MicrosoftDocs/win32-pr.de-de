---
title: IMsRdpClipboard-Schnittstelle
description: Stellt den Zwischenablagecontroller dar, der zum Synchronisieren der lokalen und Remote-Zwischenablage verwendet wird, wenn die manuelle Zwischenablagesynchronisierung aktiviert ist.
ms.tgt_platform: multiple
keywords:
- IMsRdpClipboard-Remotedesktopdienste
- IMsRdpClipboard-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a1ffc9a503365337676a11ccbdb872c1c7c7bed24eeb108fe1d565ced4de41d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606877"
---
# <a name="imsrdpclipboard-interface"></a>IMsRdpClipboard-Schnittstelle

Stellt den Zwischenablagecontroller dar, der zum Synchronisieren der lokalen und Remote-Zwischenablage verwendet wird, wenn die manuelle Zwischenablagesynchronisierung aktiviert ist (d. h., der [ManualClipboardSyncEnabled-Eigenschaftswert](imsrdpextendedsettings-property.md) ist auf **True festgelegt).**

## <a name="members"></a>Member

Die **IMsRdpClipboard-Schnittstelle** erbt von **IUnknown**. **IMsRdpClipboard** verfügt auch über diese Membertypen:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMsRdpClipboard-Schnittstelle** verfügt über diese Methoden.


| Methode        | BESCHREIBUNG      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Gibt an, ob die lokale Zwischenablage mit der Remotesitzung synchronisiert werden kann.                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Gibt an, ob die Remoteablage mit der lokalen Sitzung synchronisiert werden kann.                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Synchronisiert die lokale Zwischenablage mit der Remotesitzung.                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Synchronisiert die Remote-Zwischenablage mit der lokalen Sitzung.                      |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard ist als 2E769EE8-00C7-43DC-AFD9-235D75B72A40 definiert.            |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable7::Zwischenablage**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
