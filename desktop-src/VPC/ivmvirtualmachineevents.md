---
title: Ivmvirtualmachineevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmvirtualmachine-Schnittstelle.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Ivmvirtualmachineevents Interface Virtual PC
- Ivmvirtualmachineevents Interface Virtual PC, beschrieben
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
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478669"
---
# <a name="ivmvirtualmachineevents-interface"></a>Ivmvirtualmachineevents-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die ausgehende Ereignis Schnittstelle für die [**ivmvirtualmachine**](ivmvirtualmachine.md) -Schnittstelle. Der Client implementiert diese Methoden, um von [**ivmvirtualmachine**](ivmvirtualmachine.md)gesendete Ereignisse zu empfangen.

## <a name="members"></a>Member

Die **ivmvirtualmachineevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmvirtualmachineevents** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ivmvirtualmachineevents** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Onadditionsavailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer verfügbar sind.<br/>                                                |
| [**Onadditionsuninstalliert**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer deinstalliert werden.<br/>                                              |
| [**Onconfigurationchanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.<br/>                                        |
| [**Ondiskouesleerraum**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Empfängt eine Benachrichtigung, dass ein für eine virtuelle Maschine erforderlicher Datenträger nicht über genügend Speicherplatz verfügt und die virtuelle Maschine nicht ausgeführt werden kann.<br/>           |
| [**Onenhancedvideomode Changed**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Empfängt eine Benachrichtigung, dass die Unterstützung einer virtuellen Maschine für den erweiterten Videomodus geändert wurde.<br/>                                          |
| [**Onguestlogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Empfängt eine Benachrichtigung, dass sich ein Benutzer vom Gast Betriebssystem abgemeldet hat.<br/>                                                    |
| [**Onguestshutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Empfängt eine Benachrichtigung, dass das Gast Betriebssystem heruntergefahren wurde.<br/>                                                                     |
| [**Onheartbeatbeendet**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Empfängt eine Benachrichtigung, dass der Takt einer virtuellen Maschine beendet wurde. Dies weist normalerweise darauf hin, dass das Gast Betriebssystem abgestürzt ist.<br/> |
| [**Onrequestshutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren durchgeführt wurde.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Empfängt eine Benachrichtigung, dass ein virtueller Computer zurückgesetzt wurde.<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat.<br/>                                                                    |
| [**Ontrplefault**](ivmvirtualmachineevents-ontriplefault.md)                           | Empfängt eine Benachrichtigung, dass ein virtueller Computer einen dreifachen Fehler verursacht hat.<br/>                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.<br/>   |



 

