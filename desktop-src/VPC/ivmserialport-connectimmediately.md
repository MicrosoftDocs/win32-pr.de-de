---
title: Ivmserialport connectimmediately-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Connectimmediately-Eigenschaft virtueller PC
- Connectimmediately-Eigenschaft Virtual PC, ivmserialport-Schnittstelle
- Ivmserialport Interface Virtual PC, connectimmediately (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741744"
---
# <a name="ivmserialportconnectimmediately-property"></a>Ivmserialport:: connectimmediately (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Bestimmt, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a>Eigenschaftswert

**Variant \_ TRUE** , wenn der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird. **Variant \_ Andernfalls false** .

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                            |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>                               |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                        |



## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur gültig, wenn die [**Porttyp**](ivmserialport-type.md) -Eigenschaft **vmserialport \_ hostport** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmserialport**](ivmserialport.md)
</dt> </dl>

 

