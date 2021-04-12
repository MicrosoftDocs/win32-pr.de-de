---
title: Ivmguestos-Schnittstelle (vpccominterfaces. h)
description: Definiert das Gast Betriebssystem, das auf einem virtuellen Computer ausgeführt wird.
ms.assetid: fb31f294-94ad-4545-8d59-849a5f2fe780
keywords:
- Ivmguestos Interface Virtual PC
- Virtueller Computer für ivmguestos Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMGuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b52d4f7651a21b1baad31448e47866dfb5bf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105813"
---
# <a name="ivmguestos-interface"></a>Ivmguestos-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert das Gast Betriebssystem, das auf einem virtuellen Computer ausgeführt wird. Mit dieser Schnittstelle können Sie mit den Integrations Komponenten interagieren, die innerhalb des Gast Betriebssystems ausgeführt werden. **Ivmguestos** für eine virtuelle Maschine kann mithilfe der [**ivmvirtualmachine:: guestos**](ivmvirtualmachine-guestos.md) -Eigenschaft abgerufen werden.

## <a name="members"></a>Member

Die **ivmguestos** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmguestos** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmguestos** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                                             |
|:--------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Getosversioninfo**](ivmguestos-getosversioninfo.md)                         | Ruft Versionsinformationen für das Gast Betriebssystem ab, das auf dem virtuellen Computer ausgeführt wird.<br/> |
| [**GetParameter**](ivmguestos-getparameter.md)                                 | Ruft einen benannten Parameter innerhalb des Gasts ab.<br/>                                                |
| [**Installintegrationcomponents**](ivmguestos-installintegrationcomponents.md) | Hiermit werden die aktuellen Integrations Komponenten in das Gast Betriebssystem eingecheckt und installiert.<br/>      |
| [**Isuserloggedon**](ivmguestos-isuserloggedon.md)                             | Bestimmt, ob die angeforderte Sitzung vorhanden ist.<br/>                                         |
| [**Abmeldung**](ivmguestos-logoff.md)                                             | Protokolliert alle Benutzer vom Gast Betriebssystem.<br/>                                          |
| [**Neu starten**](ivmguestos-restart.md)                                           | Startet das Gast Betriebssystem neu.<br/>                                                         |
| [**SetParameter**](ivmguestos-setparameter.md)                                 | Legt einen benannten Parameter innerhalb des Gasts fest.<br/>                                                     |
| [**Abschlusses**](ivmguestos-shutdown.md)                                         | Fährt das Gast Betriebssystem herunter.<br/>                                                       |



 

### <a name="properties"></a>Eigenschaften

Die **ivmguestos** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                 |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanShutdown**](ivmguestos-canshutdown.md)<br/>                                   | Schreibgeschützt<br/>  | Gibt an, ob das Gast Betriebssystem ordnungsgemäß heruntergefahren werden kann (erfordert Integrations Komponenten).<br/>                         |
| [**Computername**](ivmguestos-computername.md)<br/>                                 | Schreibgeschützt<br/>  | Der Computername des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                  |
| [**CSDVersion**](ivmguestos-csdversion.md)<br/>                                     | Schreibgeschützt<br/>  | Die CSDVersion des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                     |
| [**Heartbeatprozentsatz**](ivmguestos-heartbeatpercentage.md)<br/>                   | Schreibgeschützt<br/>  | Der Prozentsatz der erwarteten Takte, die in der letzten Minute empfangen wurden.<br/>                                                             |
| [**Integrationcomponentsversion**](ivmguestos-integrationcomponentsversion.md)<br/> | Schreibgeschützt<br/>  | Die Version der Integrations Komponenten, die im Gast Betriebssystem installiert sind.<br/>                                               |
| [**Isheartbeat**](ivmguestos-isheartbeating.md)<br/>                             | Schreibgeschützt<br/>  | Gibt an, ob der virtuelle Computer über einen Takt verfügt.<br/>                                                                           |
| [**Ishosttimesyncenabled**](ivmguestos-ishosttimesyncenabled.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob die Integrations Komponenten auf diesem virtuellen Computer die Uhr des Gasts mit der hostuhr synchronisieren sollen.<br/> |
| [**Multipleusersessionsallowed**](ivmguestos-multipleusersessionsallowed.md)<br/>   | Schreibgeschützt<br/>  | Gibt an, ob mehrere Benutzersitzungen gleichzeitig im Gast Betriebssystem zulässig sind.<br/>                                 |
| [**OSBuildNumber**](ivmguestos-osbuildnumber.md)<br/>                               | Schreibgeschützt<br/>  | Die Buildnummer des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                   |
| [**OSMajorVersion**](ivmguestos-osmajorversion.md)<br/>                             | Schreibgeschützt<br/>  | Die Hauptversion des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                  |
| [**OSMinorVersion**](ivmguestos-osminorversion.md)<br/>                             | Schreibgeschützt<br/>  | Die neben Version des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                  |
| [**OSName**](ivmguestos-osname.md)<br/>                                             | Schreibgeschützt<br/>  | Der Name des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                           |
| [**OSPlatformID**](ivmguestos-osplatformid.md)<br/>                                 | Schreibgeschützt<br/>  | Der Platt Form Bezeichner des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                            |
| [**OSVersion**](ivmguestos-osversion.md)<br/>                                       | Schreibgeschützt<br/>  | Die Version des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                        |
| [**ProductType**](ivmguestos-producttype.md)<br/>                                   | Schreibgeschützt<br/>  | Der Produkttyp des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                   |
| [**Screenlock**](ivmguestos-screenlocked.md)<br/>                                 | Schreibgeschützt<br/>  | Gibt an, ob der Bildschirm im Gast Betriebssystem gesperrt ist.<br/>                                                            |
| [**Servicepackmajor**](ivmguestos-servicepackmajor.md)<br/>                         | Schreibgeschützt<br/>  | Die Hauptversion der Service Pack des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                              |
| [**Servicepackminor**](ivmguestos-servicepackminor.md)<br/>                         | Schreibgeschützt<br/>  | Die neben Version der Service Pack des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                              |
| [**Suitemask**](ivmguestos-suitemask.md)<br/>                                       | Schreibgeschützt<br/>  | Der suitemask des Gast Betriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                      |
| [**Terminalserverport**](ivmguestos-terminalserverport.md)<br/>                     | Schreibgeschützt<br/>  | Port, der von Remotedesktopdienste im Gast Betriebssystem verwendet wird.<br/>                                                              |
| [**Terminalservicesinitialisiert**](ivmguestos-terminalservicesinitialized.md)<br/>   | Schreibgeschützt<br/>  | Der Status der terminaldiensteinitialisierung im Gast Betriebssystem.<br/>                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



 

