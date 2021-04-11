---
title: IMsRdpClipboard-Schnittstelle
description: Stellt den Zwischenablage Controller dar, mit dem die lokalen und Remote-zwischen Ablagen synchronisiert werden, wenn die manuelle Synchronisierung der Zwischenablage aktiviert
ms.tgt_platform: multiple
keywords:
- Imsrdpclipboard-Schnittstelle Remotedesktopdienste
- Imsrdpclipboard-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123301"
---
# <a name="imsrdpclipboard-interface"></a>IMsRdpClipboard-Schnittstelle

Stellt den Zwischenablage Controller dar, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Synchronisierung der Zwischenablage aktiviert ist (d. h., der [manualclipboardsyncenabled](imsrdpextendedsettings-property.md) -Eigenschafts Wert ist auf **true**

## <a name="members"></a>Member

Die **imsrdpclipboard** -Schnittstelle erbt von **IUnknown**. **Imsrdpclipboard** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imsrdpclipboard** -Schnittstelle verfügt über diese Methoden.


| Methode        | BESCHREIBUNG      |
|:---------------|:----------------|
| [**Cansynclocalclipboardtor emotesession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Gibt an, ob die lokale Zwischenablage mit der Remote Sitzung synchronisiert werden kann.                   |
| [**Cansynkremoteclipboardtolocalsession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Gibt an, ob die Remote Zwischenablage mit der lokalen Sitzung synchronisiert werden kann.                   |
| [**Synclocalclipboardtor emotesession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Synchronisiert die lokale Zwischenablage mit der Remote Sitzung.                   |
| [**Synkremoteclipboardtolocalsession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Synchronisiert die Remote Zwischenablage mit der lokalen Sitzung.                      |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ imsrdpclipboard ist als 2e769ee8-00c7-43dc-afd9-235d75b72a40 definiert.            |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable7:: Zwischenablage**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
