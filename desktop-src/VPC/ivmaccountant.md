---
title: Ivmaccountant-Schnittstelle (vpccominterfaces. h)
description: Ermöglicht den Zugriff auf Buchhaltungs bezogene Informationen für einen virtuellen Computer.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Ivmaccountant Interface Virtual PC
- Ivmaccountant Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743473"
---
# <a name="ivmaccountant-interface"></a>Ivmaccountant-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ermöglicht den Zugriff auf Buchhaltungs bezogene Informationen für einen virtuellen Computer. Zum Abrufen des **ivmaccountant** für eine virtuelle Maschine verwenden Sie die [**ivmvirtualmachine:: Accountant**](ivmvirtualmachine-accountant.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmaccountant** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmaccountant** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmaccountant** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp          | BESCHREIBUNG                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**CPU**](ivmaccountant-cpuutilization.md)<br/>               | Schreibgeschützt<br/> | Der Prozentsatz der aktuellen CPU-Auslastung für diese virtuelle Maschine.<br/>                          |
| [**Cpuutilizationhistory**](ivmaccountant-cpuutilizationhistory.md)<br/> | Schreibgeschützt<br/> | Die aktuelle CPU-Auslastung dieses virtuellen Computers (als Array von Prozentwerten).<br/>       |
| [**Diskbytesread**](ivmaccountant-diskbytesread.md)<br/>                 | Schreibgeschützt<br/> | Die Gesamtanzahl der von allen Speicher Controllern für diesen virtuellen Computer gelesenen Bytes.<br/>          |
| [**Diskbytesgeschrieben**](ivmaccountant-diskbyteswritten.md)<br/>           | Schreibgeschützt<br/> | Die Gesamtanzahl der Bytes, die von allen Speicher Controllern für diesen virtuellen Computer geschrieben wurden.<br/>       |
| [**Networkbytesempfangene**](ivmaccountant-networkbytesreceived.md)<br/>   | Schreibgeschützt<br/> | Die Gesamtanzahl der Bytes, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen wurden.<br/> |
| [**Network bytess**](ivmaccountant-networkbytessent.md)<br/>           | Schreibgeschützt<br/> | Die Gesamtanzahl der Bytes, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer gesendet werden.<br/>     |
| [**Betriebszeit**](ivmaccountant-uptime.md)<br/>                               | Schreibgeschützt<br/> | Die Anzahl der Sekunden, die der virtuelle Computer ausgeführt wurde.<br/>                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.<br/>              |



 

