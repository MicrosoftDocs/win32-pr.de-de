---
title: IVMGuestOS-HeartbeatPercentage-Eigenschaft (VPCCOMInterfaces.h)
description: Prozentsatz der erwarteten Heartbeats, die in der letzten Minute empfangen wurden.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- HeartbeatPercentage-Eigenschaft Virtueller PC
- HeartbeatPercentage-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, HeartbeatPercentage-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1415b9d59e28e5658dc5b54a1a6d118e0b12a77b3208978448afb2b336f313e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753447"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>IVMGuestOS::HeartbeatPercentage-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Prozentsatz der erwarteten Takte ab, die in der letzten Minute empfangen wurden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Prozentsatz der erwarteten Takte, die in der letzten Minute empfangen wurden.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                              | Bedeutung                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | Der Vorgang wurde durchgeführt.<br/>                                                                                                            |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                   | Der Parameter ist **NULL.**<br/>                                                                                                               |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | Die Konfiguration ist unbekannt.<br/>                                                                                                            |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl>      | Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.<br/>                                                                             |
| <dl> <dt>VM \_ \_E ADDITIONEN \_ NICHT \_ VERFÜGBAR</dt> <dt>0xA0040504</dt> </dl> | Der virtuelle Computer ist nicht vollständig gestartet, das Integrationskomponentenfeature ist nicht installiert, oder die installierte Version unterstützt dieses Feature nicht.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                        |



## <a name="remarks"></a>Hinweise

Integrationskomponenten senden einen periodischen Heartbeat an Windows Virtual PC, während das Gastbetriebssystem ausgeführt wird. Wenn das Gastbetriebssystem stark ausgelastet ist, ist es möglich, dass Windows Virtueller PC weniger Takte empfängt als erwartet. Wenn der Heartbeatprozentsatz auf 0 (null) fällt, reagiert das Gastbetriebssystem möglicherweise nicht oder stürzt ab. Der virtuelle Computer muss ausgeführt werden (d. h. vollständig gestartet und nicht heruntergefahren werden), und Integrationskomponenten müssen installiert werden, wenn diese Eigenschaft aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

