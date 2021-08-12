---
title: IVMGuestOS-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert das Gastbetriebssystem, das auf einem virtuellen Computer ausgeführt wird.
ms.assetid: fb31f294-94ad-4545-8d59-849a5f2fe780
keywords:
- IVMGuestOS-Schnittstelle Virtueller PC
- IVMGuestOS-Schnittstelle Virtueller PC , beschrieben
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
ms.openlocfilehash: 51a36c6c579209903c45e3888a11f17d40c168bbb2e215c60fb25e5b12330962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593998"
---
# <a name="ivmguestos-interface"></a>IVMGuestOS-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert das Gastbetriebssystem, das auf einem virtuellen Computer ausgeführt wird. Mit dieser Schnittstelle können Sie mit den Integrationskomponenten interagieren, die im Gastbetriebssystem ausgeführt werden. **IVMGuestOS** für einen virtuellen Computer kann mithilfe der [**IVMVirtualMachine::GuestOS-Eigenschaft**](ivmvirtualmachine-guestos.md) abgerufen werden.

## <a name="members"></a>Member

Die **IVMGuestOS-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMGuestOS** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMGuestOS-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                                             |
|:--------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetOsVersionInfo**](ivmguestos-getosversioninfo.md)                         | Ruft Versionsinformationen für das Gastbetriebssystem ab, das auf dem virtuellen Computer ausgeführt wird.<br/> |
| [**Dbparametercollection.getparameter**](ivmguestos-getparameter.md)                                 | Ruft einen benannten Parameter innerhalb des Gasts ab.<br/>                                                |
| [**InstallIntegrationComponents**](ivmguestos-installintegrationcomponents.md) | Sucht und installiert die neuesten Integrationskomponenten im Gastbetriebssystem.<br/>      |
| [**IsUserLoggedOn**](ivmguestos-isuserloggedon.md)                             | Bestimmt, ob die angeforderte Sitzung vorhanden ist.<br/>                                         |
| [**Abmelden**](ivmguestos-logoff.md)                                             | Meldet alle Benutzer vom Gastbetriebssystem ab.<br/>                                          |
| [**Neu starten**](ivmguestos-restart.md)                                           | Startet das Gastbetriebssystem neu.<br/>                                                         |
| [**Dbparametercollection.setparameter**](ivmguestos-setparameter.md)                                 | Legt einen benannten Parameter innerhalb des Gasts fest.<br/>                                                     |
| [**Herunterfahren**](ivmguestos-shutdown.md)                                         | Fährt das Gastbetriebssystem herunter.<br/>                                                       |



 

### <a name="properties"></a>Eigenschaften

Die **IVMGuestOS-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                 |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canshutdown**](ivmguestos-canshutdown.md)<br/>                                   | Schreibgeschützt<br/>  | Gibt an, ob das Gastbetriebssystem sauber heruntergefahren werden kann (erfordert Integrationskomponenten).<br/>                         |
| [**ComputerName**](ivmguestos-computername.md)<br/>                                 | Schreibgeschützt<br/>  | Der Computername des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                  |
| [**CSDVersion**](ivmguestos-csdversion.md)<br/>                                     | Schreibgeschützt<br/>  | Die CSDVersion des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                     |
| [**HeartbeatPercentage**](ivmguestos-heartbeatpercentage.md)<br/>                   | Schreibgeschützt<br/>  | Der Prozentsatz der erwarteten Takte, die in der letzten Minute empfangen wurden.<br/>                                                             |
| [**IntegrationComponentsVersion**](ivmguestos-integrationcomponentsversion.md)<br/> | Schreibgeschützt<br/>  | Die Version der Im Gastbetriebssystem installierten Integrationskomponenten.<br/>                                               |
| [**IsHeartbeating**](ivmguestos-isheartbeating.md)<br/>                             | Schreibgeschützt<br/>  | Gibt an, ob der virtuelle Computer über einen Heartbeat verfügt.<br/>                                                                           |
| [**IsHostTimeSyncEnabled**](ivmguestos-ishosttimesyncenabled.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob die Integrationskomponenten auf diesem virtuellen Computer die Uhr des Gasts mit der Uhr des Hosts synchronisieren sollen.<br/> |
| [**MultipleUserSessionsAllowed**](ivmguestos-multipleusersessionsallowed.md)<br/>   | Schreibgeschützt<br/>  | Gibt an, ob mehrere gleichzeitige Benutzersitzungen im Gastbetriebssystem zulässig sind.<br/>                                 |
| [**OSBuildNumber**](ivmguestos-osbuildnumber.md)<br/>                               | Schreibgeschützt<br/>  | Die Buildnummer des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                   |
| [**OSMajorVersion**](ivmguestos-osmajorversion.md)<br/>                             | Schreibgeschützt<br/>  | Die Hauptversion des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                  |
| [**OSMinorVersion**](ivmguestos-osminorversion.md)<br/>                             | Schreibgeschützt<br/>  | Die Nebenversion des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                  |
| [**OSName**](ivmguestos-osname.md)<br/>                                             | Schreibgeschützt<br/>  | Der Name des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                           |
| [**OSPlatformId**](ivmguestos-osplatformid.md)<br/>                                 | Schreibgeschützt<br/>  | Der Plattformbezeichner des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                            |
| [**OSVersion**](ivmguestos-osversion.md)<br/>                                       | Schreibgeschützt<br/>  | Die Version des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                        |
| [**ProductType**](ivmguestos-producttype.md)<br/>                                   | Schreibgeschützt<br/>  | Der Produkttyp des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                   |
| [**ScreenLocked**](ivmguestos-screenlocked.md)<br/>                                 | Schreibgeschützt<br/>  | Gibt an, ob der Bildschirm im Gastbetriebssystem gesperrt ist.<br/>                                                            |
| [**ServicePackMajor**](ivmguestos-servicepackmajor.md)<br/>                         | Schreibgeschützt<br/>  | Die Hauptversion des Service Packs des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                              |
| [**ServicePackMinor**](ivmguestos-servicepackminor.md)<br/>                         | Schreibgeschützt<br/>  | Die Nebenversion des Service Packs des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                              |
| [**SuiteMask**](ivmguestos-suitemask.md)<br/>                                       | Schreibgeschützt<br/>  | Die SuiteMask des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.<br/>                                                      |
| [**TerminalServerPort**](ivmguestos-terminalserverport.md)<br/>                     | Schreibgeschützt<br/>  | Port, der von Remotedesktopdienste im Gastbetriebssystem verwendet wird.<br/>                                                              |
| [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md)<br/>   | Schreibgeschützt<br/>  | Der Status der Terminaldiensteinitialisierung im Gastbetriebssystem.<br/>                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



 

