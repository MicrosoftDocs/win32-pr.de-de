---
title: IMsRdpCameraRedirConfig-Schnittstelle
description: Stellt die Konfigurationen für eine Kamera dar, die für die Umleitung verfügbar ist.
ms.tgt_platform: multiple
keywords:
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520307"
---
# <a name="imsrdpcameraredirconfig-interface"></a>IMsRdpCameraRedirConfig-Schnittstelle

Stellt die Konfigurationen für eine Kamera dar, die für die Umleitung verfügbar ist.

## <a name="members"></a>Member

Die **imsrdpcameraredirconfig** -Schnittstelle erbt von **IUnknown**. **Imsrdpcameraredirconfig** verfügt auch über die folgenden Typen von Membern:

- [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **imsrdpcameraredirconfig** -Schnittstelle verfügt über diese Eigenschaften.

| Eigenschaft         | Zugriffstyp           | BESCHREIBUNG            |
|:-----------------|:----------------------|:-----------------------|
| [**Deviceexistiert**](imsrdpcameraredirconfig-deviceexists.md)      | Schreibgeschützt | Gibt an, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Schreibgeschützt |    Ruft den anzeigen amen der Kamera ab.    |
| [**InstanceId**](imsrdpcameraredirconfig-instanceid.md)      | Schreibgeschützt |  Ruft die Instanz-ID der Kamera ab.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Schreibgeschützt |    Ruft die Instanz-ID der übergeordneten Instanz der Kamera ab.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Lesen/Schreiben |  Gibt an, ob die Kamera umgeleitet wird oder nicht.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Schreibgeschützt |   Ruft den symbolischen Link der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera ab.   |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.            |

## <a name="see-also"></a>Siehe auch

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7:: cameraredirconfigcollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)