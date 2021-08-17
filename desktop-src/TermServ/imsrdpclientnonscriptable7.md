---
title: IMsRdpClientNonScriptable7-Schnittstelle
description: Ermöglicht den Zugriff auf die nicht beschreibbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable6-Schnittstelle abgeleitet.
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable7-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable7-Schnittstelle Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 01065ef73d1a23f0ac9416a39c4af74042c883e3b4d7f596cb95f6c01043f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941107"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>IMsRdpClientNonScriptable7-Schnittstelle

Ermöglicht den Zugriff auf die nicht beschreibbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der [**IMsRdpClientNonScriptable6-Schnittstelle**](imsrdpclientnonscriptable6.md) abgeleitet. Auf Methoden dieser Schnittstelle kann nur über die vtable zugegriffen werden. Sie sind nicht für die Verwendung für skriptfähige Clients verfügbar.

Eine Instanz dieser Schnittstelle wird durch Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das [**IMsTscAx-Objekt**](imstscax-interface.md) abgerufen, wobei **\_ IID-IMsRdpClientNonScriptable7** übergeben werden.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable7-Schnittstelle** erbt von [**IMsRdpClientNonScriptable6.**](imsrdpclientnonscriptable5.md) **IMsRdpClientNonScriptable7** verfügt auch über diese Typen von Membern:

- [Methoden](#methods)
- [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClientNonScriptable7-Schnittstelle** verfügt über diese Methoden.


| Methode            | Beschreibung              |
|:------------------|:-------------------------|
| [**DisableDpiCursorScalingForProcess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Deaktiviert die lokale Skalierung des vom Server empfangenen Mauszeigers und stellt sicher, dass die Cursorform ohne Änderungen ordnungsgemäß gerendert wird.                   |

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable7-Schnittstelle** verfügt über diese Eigenschaften.

| Eigenschaft         | Zugriffstyp           | Beschreibung            |
|:-----------------|:----------------------|:-----------------------|
| [**CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Schreibgeschützt |  Ruft die Auflistung der Kameras (und der zugehörigen Konfigurationen) ab, die für die Umleitung verfügbar sind.   |
| [**Zwischenablage**](imsrdpclientnonscriptable7-clipboard.md)                       | Schreibgeschützt |    Ruft den Zwischenablagecontroller ab, der zum Synchronisieren der lokalen und Remotezwischenablage verwendet wird, wenn die manuelle Synchronisierung der Zwischenablage aktiviert ist.    |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1803 (Build 17134)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 ist als 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8 definiert.<br/> CLSID \_ MsRdpClient12NotSafeForScripting ist als 3BB805C2-D9E2-4174-8A1E-C87D69563662 definiert.<br/> CLSID \_ MsRdpClient11 ist als 22A7E88C-5BF5-4DE6-B687-60F7331DF190 definiert.<br/> CLSID \_ MsRdpClient11NotSafeForScripting ist als 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8 definiert.<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 ist als 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC definiert.            |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
