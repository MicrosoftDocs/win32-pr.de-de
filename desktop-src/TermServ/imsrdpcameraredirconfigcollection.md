---
title: IMsRdpCameraRedirConfigCollection-Schnittstelle
description: Stellt die Auflistung der Kameras (und der zugeordneten Konfigurationen) dar, die für die Umleitung verfügbar sind.
ms.tgt_platform: multiple
keywords:
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123283"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>IMsRdpCameraRedirConfigCollection-Schnittstelle

 Stellt die Auflistung der Kameras (und der zugeordneten Konfigurationen) dar, die für die Umleitung verfügbar sind.

## <a name="members"></a>Member

Die **imsrdpcameraredirconfigcollection** -Schnittstelle erbt von **IUnknown**. **Imsrdpcameraredirconfigcollection** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)
- [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **imsrdpcameraredirconfigcollection** -Schnittstelle verfügt über diese Methoden.

| Methode            | BESCHREIBUNG              |
|:------------------|:-------------------------|
| [**AddConfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Fügt der Auflistung ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt hinzu (die entsprechende Kamera muss nicht verbunden sein).                   |
| [**Neu einlesen**](imsrdpcameraredirconfigcollection-rescan.md)       |  Listet verbundene Kamerageräte auf.                   |

### <a name="properties"></a>Eigenschaften

Die **imsrdpcameraredirconfigcollection** -Schnittstelle verfügt über diese Eigenschaften.

| Eigenschaft         | Zugriffstyp           | BESCHREIBUNG            |
|:-----------------|:----------------------|:-----------------------|
| [**Byindex**](imsrdpcameraredirconfigcollection-byindex.md)      | Schreibgeschützt |  Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt nach dem Index in der Auflistung zurück.   |
| [**Byinstanceid**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Schreibgeschützt |    Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.    |
| [**Bysymboliclink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Schreibgeschützt |  Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen symbolischen Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera entspricht.  |
| [**Countdown**](imsrdpcameraredirconfigcollection-count.md)                       | Schreibgeschützt |    Gibt die Anzahl der [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekte in der Auflistung zurück.   |
| [**Encode Video**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Lesen/Schreiben |  Gibt an, ob der Videostream H. 264-codiert ist.  |
| [**Encodingquality**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Lesen/Schreiben |    Gibt die Codierungsqualität an (Bitrate).   |
| [**Redirectbydefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Lesen/Schreiben |   Gibt an, ob eine neue Kamera standardmäßig umgeleitet wird.    |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.            |

## <a name="see-also"></a>Siehe auch

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7:: cameraredirconfigcollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
