---
title: IMsRdpClientNonScriptable7-Schnittstelle
description: Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable6-Schnittstelle abgeleitet.
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable7-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable7 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106345572"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>IMsRdpClientNonScriptable7-Schnittstelle

Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) -Schnittstelle abgeleitet. Auf Methoden dieser Schnittstelle kann nur über die Vtable zugegriffen werden. Sie sind nicht zur Verwendung mit Skript fähigen Clients verfügbar.

Eine Instanz dieser Schnittstelle wird durch Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das [**imstscax**](imstscax-interface.md) -Objekt abgerufen, wobei **IID \_ IMsRdpClientNonScriptable7** übergeben wird.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable7** -Schnittstelle erbt von [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable7** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)
- [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClientNonScriptable7** -Schnittstelle verfügt über diese Methoden.


| Methode            | BESCHREIBUNG              |
|:------------------|:-------------------------|
| [**Disabledpicurrsorscalingforprocess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Deaktiviert die lokale Skalierung des Mauszeigers, der vom Server empfangen wurde. Dadurch wird sichergestellt, dass die Cursor Form ohne Änderung korrekt gerendert wird.                   |

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable7** -Schnittstelle verfügt über diese Eigenschaften.

| Eigenschaft         | Zugriffstyp           | BESCHREIBUNG            |
|:-----------------|:----------------------|:-----------------------|
| [**Cameraredirconfigcollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Schreibgeschützt |  Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.   |
| [**Zwischenablage**](imsrdpclientnonscriptable7-clipboard.md)                       | Schreibgeschützt |    Ruft den Zwischenablage Controller ab, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert    |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | Die CLSID- \_ MsRdpClient12 ist als 0bda33b8-9af1-4065-989e-5a7f 1acb09d8 definiert.<br/> CLSID \_ MsRdpClient12NotSafeForScripting ist als 3bb805c2-d9e2-4174-8a1e-c87d69563662 definiert<br/> CLSID \_ MsRdpClient11 ist als 22a7e88c-5bf 5-4de6-B687-60b7331df190 definiert.<br/> CLSID \_ MsRdpClient11NotSafeForScripting ist als 1df7c823-b2d4-4b54-975a-f2ac5d7cf8b8 definiert.<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 ist als 71b4a60a-fe21-46d8-a39b-8e32ba0c5ecc definiert.            |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
