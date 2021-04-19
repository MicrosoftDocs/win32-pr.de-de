---
title: Ivmguestos isheartangeschlagen-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der virtuelle Computer über einen Takt verfügt.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Isheartangeschlagen-Eigenschaft virtueller PC
- Isheartangeschlagen-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, isheartangeschlagen (Eigenschaft)
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
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342666"
---
# <a name="ivmguestosisheartbeating-property"></a>Ivmguestos:: isheartangeschlagen (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Bestimmt, ob der virtuelle Computer über einen Takt verfügt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Eigenschaftswert

**Variant \_ "True** ", wenn ein Takt erkannt wird, andernfalls " **\_ false** ".

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                              | Bedeutung                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | Der Vorgang wurde durchgeführt.<br/>                                                                                                                         |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                   | Der-Parameter ist **null**.<br/>                                                                                                                            |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>           | Die Konfiguration ist unbekannt.<br/>                                                                                                                         |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl>      | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                                                                                               |
| <dl> <dt>VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch</dt> nehmen <dt>0xa0040504</dt> </dl> | Der virtuelle Computer wurde nicht vollständig gestartet, das Feature für die Integrations Komponenten ist nicht installiert, oder die installierte Version unterstützt diese Funktion nicht.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                     |



## <a name="remarks"></a>Bemerkungen

Wenn Integrations Komponenten im Gast Betriebssystem installiert sind, wird ein regulärer Takt oder Takt von der Sitzung der virtuellen Maschine an Windows Virtual PC gesendet. Wenn das Gast Betriebssystem stark ausgelastet ist, wird es möglich sein, dass der virtuelle PC weniger Takte als erwartet empfängt. Wenn kein Takt erkannt wird, reagiert das Gast Betriebssystem möglicherweise nicht oder ist abgestürzt.

Standardmäßig erzeugt ein virtueller Computer zehn Takt Ticks pro Minute. Wenn für eine ganze Minute keine Takt Takte erkannt werden, versucht Windows Virtual PC, die Sitzung für virtuelle Maschinen alle zehn Sekunden bis zu zwei Minuten neu zu starten. Dieses Verhalten wird durch die folgenden Schlüsselwerte in der Konfigurationsdatei der Sitzung der virtuellen Maschine gesteuert.



| Konfigurationsschlüssel                                            | Standard       | BESCHREIBUNG                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Integration/Microsoft/Heartbeat/Zeit<br/>              | 60<br/> | Die Länge des Zeit Blocks, der zum Generieren von Takt Ticks verwendet wird (in Sekunden).<br/>                                             |
| Integration/Microsoft/Heartbeat/Rate<br/>              | 10<br/> | Die Anzahl der Ticks, die in jedem Takt Zeit Block generiert werden.<br/>                                                                  |
| Integration/Microsoft/Heartbeat/Fehler \_ Intervall<br/> | 10<br/> | Die Anzahl der Sekunden zwischen Neustart versuchen, sobald keine Takt Ticks innerhalb eines bestimmten Takt Zeit Blocks empfangen werden.<br/> |
| Integration/Microsoft/Heartbeat/Fehler \_ Versuche<br/> | 12<br/> | Die Anzahl der erfolgten Neustart Versuche.<br/>                                                                                         |



 

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

 

