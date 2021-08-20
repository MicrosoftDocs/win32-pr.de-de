---
title: IVMVirtualMachineEvents-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die ausgehende Ereignisschnittstelle für die IVMVirtualMachine-Schnittstelle.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6686585333f33d4732284ab448a82ac722fea03315b08aaa276f2eeabaf2e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122620"
---
# <a name="ivmvirtualmachineevents-interface"></a>IVMVirtualMachineEvents-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die ausgehende Ereignisschnittstelle für die [**IVMVirtualMachine-Schnittstelle.**](ivmvirtualmachine.md) Der Client implementiert diese Methoden zum Empfangen von Ereignissen, die von [**IVMVirtualMachine**](ivmvirtualmachine.md)gesendet werden.

## <a name="members"></a>Member

Die **IVMVirtualMachineEvents-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualMachineEvents** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IVMVirtualMachineEvents-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Empfängt eine Benachrichtigung, dass Integrationskomponenten auf einem virtuellen Computer verfügbar sind.<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Empfängt die Benachrichtigung, dass Integrationskomponenten auf einem virtuellen Computer deinstalliert werden.<br/>                                              |
| [**OnConfigurationChanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Empfängt die Benachrichtigung, dass ein für einen virtuellen Computer erforderlicher Datenträger nicht verfügbar ist und der virtuelle Computer nicht ausgeführt werden kann.<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Empfängt eine Benachrichtigung, dass sich die Unterstützung eines virtuellen Computers für den erweiterten Videomodus geändert hat.<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Empfängt die Benachrichtigung, dass sich ein Benutzer vom Gastbetriebssystem abgemeldet hat.<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Empfängt die Benachrichtigung, dass das Gastbetriebssystem heruntergefahren wurde.<br/>                                                                     |
| [**OnHeartbeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Empfängt die Benachrichtigung, dass der Heartbeat eines virtuellen Computers beendet wurde. Dies weist in der Regel darauf hin, dass das Gastbetriebssystem abgestürzt ist.<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren erfolgt ist.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Empfängt eine Benachrichtigung, dass ein virtueller Computer zurückgesetzt wurde.<br/>                                                                         |
| [**Onstatechange**](ivmvirtualmachineevents-onstatechange.md)                           | Empfängt eine Benachrichtigung, dass sich der Zustand eines virtuellen Computers geändert hat.<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | Empfängt eine Benachrichtigung, dass für einen virtuellen Computer ein Dreifachfehler aufgetreten ist.<br/>                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents ist als 9d84f560-bb67-4961-bd12-a4da780c67e4 definiert.<br/>   |



 

