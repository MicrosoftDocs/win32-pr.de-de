---
title: IMsRdpCameraRedirConfig-Schnittstelle
description: Stellt die Konfigurationen für eine Kamera dar, die für die Umleitung verfügbar ist.
ms.tgt_platform: multiple
keywords:
- IMsRdpCameraRedirConfig-Schnittstelle Remotedesktopdienste
- IMsRdpCameraRedirConfig-Schnittstelle Remotedesktopdienste beschrieben
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
ms.openlocfilehash: aa030d462a16eacd521709c5be534f3d90e14f446da519490ee62f0260766084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574540"
---
# <a name="imsrdpcameraredirconfig-interface"></a>IMsRdpCameraRedirConfig-Schnittstelle

Stellt die Konfigurationen für eine Kamera dar, die für die Umleitung verfügbar ist.

## <a name="members"></a>Member

Die **IMsRdpCameraRedirConfig-Schnittstelle** erbt von **IUnknown.** **IMsRdpCameraRedirConfig** verfügt auch über diese Typen von Membern:

- [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpCameraRedirConfig-Schnittstelle** verfügt über diese Eigenschaften.

| Eigenschaft         | Zugriffstyp           | Beschreibung            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | Schreibgeschützt | Gibt an, ob das Kameragerät derzeit vorhanden ist (d.b. die Kamera ist verbunden).   |
| [**Friendlyname**](imsrdpcameraredirconfig-friendlyname.md)                       | Schreibgeschützt |    Ruft den Anzeigenamen der Kamera ab.    |
| [**Instanceid**](imsrdpcameraredirconfig-instanceid.md)      | Schreibgeschützt |  Ruft die Instanz-ID der Kamera ab.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Schreibgeschützt |    Ruft die INSTANZ-ID des übergeordneten Geräts der Kamera ab.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Lesen/Schreiben |  Gibt an, ob die Kamera umgeleitet wird.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Schreibgeschützt |   Ruft die symbolische Verknüpfung der **KSCATEGORY_VIDEO_CAMERA-Schnittstelle** für die Kamera ab.   |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig ist als 09750604-D625-47C1-9FCD-F09F735705D7 definiert.            |

## <a name="see-also"></a>Siehe auch

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)