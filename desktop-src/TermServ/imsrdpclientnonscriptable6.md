---
title: IMsRdpClientNonScriptable6-Schnittstelle
description: Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable5-Schnittstelle abgeleitet.
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable6-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable6 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104392326"
---
# <a name="imsrdpclientnonscriptable6-interface"></a>IMsRdpClientNonScriptable6-Schnittstelle

Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) -Schnittstelle abgeleitet. Auf Methoden dieser Schnittstelle kann nur über die Vtable zugegriffen werden. Sie sind nicht zur Verwendung mit Skript fähigen Clients verfügbar.

Eine Instanz dieser Schnittstelle wird durch Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das [**imstscax**](imstscax-interface.md) -Objekt abgerufen, wobei **IID \_ IMsRdpClientNonScriptable6** übergeben wird.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable6** -Schnittstelle erbt von [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable6** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMsRdpClientNonScriptable6** -Schnittstelle verfügt über diese Methoden.


| Methode            | BESCHREIBUNG                   |
|:-----------------------------|:-----------------|
| [**SendLocation2D**](imsrdpclientnonscriptable6-sendlocation2d.md)     |  Sendet einen breiten-und Längengrad Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.                   |
| [**SendLocation3D**](imsrdpclientnonscriptable6-sendlocation3d.md)     | Sendet einen breiten-, Längen-und Höhen Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.                 |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------|
| Unterstützte Mindestversion (Client)| Windows 10, Version 1709 (Build 16299)      |
| Typbibliothek            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | Die CLSID- \_ MsRdpClient12 ist als 0bda33b8-9af1-4065-989e-5a7f 1acb09d8 definiert.<br/> CLSID \_ MsRdpClient12NotSafeForScripting ist als 3bb805c2-d9e2-4174-8a1e-c87d69563662 definiert<br/> CLSID \_ MsRdpClient11 ist als 22a7e88c-5bf 5-4de6-B687-60b7331df190 definiert.<br/> CLSID \_ MsRdpClient11NotSafeForScripting ist als 1df7c823-b2d4-4b54-975a-f2ac5d7cf8b8 definiert.<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable6 ist als 05293249-B28B-4db8-BE64-1b2t496b910e definiert.            |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>
