---
title: Ivmguestos heartbeatprozent-Eigenschaft (vpccominterfaces. h)
description: Der Prozentsatz der erwarteten Takte, die in der letzten Minute empfangen wurden.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Eigenschaft "heartbeatprozent" für Virtual PC
- Eigenschaft "heartbeatprozent" Virtual PC, ivmguestos Interface
- Ivmguestos Interface Virtual PC, Eigenschaft "heartbeatprozentsatz"
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
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518800"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>Ivmguestos:: heartbeatprozent (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                   | Der-Parameter ist **null**.<br/>                                                                                                               |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>           | Die Konfiguration ist unbekannt.<br/>                                                                                                            |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl>      | Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.<br/>                                                                             |
| <dl> <dt>VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch</dt> nehmen <dt>0xa0040504</dt> </dl> | Der virtuelle Computer wurde nicht vollständig gestartet, das Feature für die Integrations Komponenten ist nicht installiert, oder die installierte Version unterstützt diese Funktion nicht.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                        |



## <a name="remarks"></a>Bemerkungen

Integrations Komponenten senden regelmäßig Taktfrequenz an Windows Virtual PC, während das Gast Betriebssystem ausgeführt wird. Wenn das Gast Betriebssystem stark ausgelastet ist, wird es möglich sein, dass Windows Virtual PC weniger Takte als erwartet empfängt. Fällt der Takt Prozentsatz auf NULL, ist es möglich, dass das Gast Betriebssystem nicht reagiert oder abgestürzt ist. Der virtuelle Computer muss ausgeführt werden (d. h. vollständig gestartet und nicht heruntergefahren werden), und Integrations Komponenten müssen installiert werden, wenn diese Eigenschaft aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmguestos**](ivmguestos.md)
</dt> </dl>

 

