---
title: IVMGuestOS IsHeartbeating-Eigenschaft (VPCCOMInterfaces.h)
description: Bestimmt, ob der virtuelle Computer über einen Takt verfügt.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- IsHeartbeating-Eigenschaft Virtueller PC
- IsHeartbeating-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC , IsHeartbeating-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91598284d3765c5ff6de185ca0cf3b652036c226d80b0fe01a9944a9d7480b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594180"
---
# <a name="ivmguestosisheartbeating-property"></a>IVMGuestOS::IsHeartbeating-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob der virtuelle Computer über einen Takt verfügt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Eigenschaftswert

**VARIANT \_ TRUE,** wenn ein Heartbeat erkannt wird, **andernfalls VARIANT \_ FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                              | Bedeutung                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | Der Vorgang wurde durchgeführt.<br/>                                                                                                                         |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                   | Der Parameter ist **NULL.**<br/>                                                                                                                            |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | Die Konfiguration ist unbekannt.<br/>                                                                                                                         |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT</dt> <dt>0xA0040206</dt> </dl>      | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                                                                                               |
| <dl> <dt>VM \_ \_E ADDITIONEN \_ NICHT \_ VERFÜGBAR</dt> <dt>0xA0040504</dt> </dl> | Der virtuelle Computer ist nicht vollständig gestartet, die Integrationskomponentenfunktion ist nicht installiert, oder die installierte Version unterstützt dieses Feature nicht.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                     |



## <a name="remarks"></a>Bemerkungen

Wenn Integrationskomponenten im Gastbetriebssystem installiert sind, wird ein regulärer Takt oder Heartbeat von der Sitzung des virtuellen Computers an Windows Virtueller PC gesendet. Wenn das Gastbetriebssystem stark ausgelastet ist, erhält der virtuelle PC möglicherweise weniger Takte als erwartet. Wenn kein Heartbeat erkannt wird, ist es möglich, dass das Gastbetriebssystem nicht reagiert oder abstürzt.

Standardmäßig erzeugt ein virtueller Computer zehn Takttakte pro Minute. Wenn für eine ganze Minute keine Takte erkannt werden, versucht Windows Virtual PC, die Sitzung des virtuellen Computers einmal alle zehn Sekunden für bis zu zwei Minuten neu zu starten. Dieses Verhalten wird durch die folgenden Schlüsselwerte in der Konfigurationsdatei der Sitzung des virtuellen Computers gesteuert.



| Konfigurationsschlüssel                                            | Standard       | BESCHREIBUNG                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| integration/microsoft/heartbeat/time<br/>              | 60<br/> | Die Länge des Zeitblocks, der zum Generieren von Takt-Ticks in Sekunden verwendet wird.<br/>                                             |
| integration/microsoft/heartbeat/rate<br/>              | 10<br/> | Die Anzahl von Ticks, die in jedem Taktzeitblock generiert werden.<br/>                                                                  |
| integration/microsoft/heartbeat/failure \_ interval<br/> | 10<br/> | Die Anzahl von Sekunden zwischen Neustartversuchen, sobald innerhalb eines bestimmten Taktzeitblocks keine Takte empfangen werden.<br/> |
| integration/microsoft/heartbeat/failure \_ attempts<br/> | 12<br/> | Die Anzahl von Neustartversuchen.<br/>                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

