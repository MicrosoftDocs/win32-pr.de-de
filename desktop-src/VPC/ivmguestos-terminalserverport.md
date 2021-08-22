---
title: IVMGuestOS TerminalServerPort-Eigenschaft
description: Port, der von Remotedesktopdienste im Gastbetriebssystem verwendet wird.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- TerminalServerPort-Eigenschaft Virtueller PC
- TerminalServerPort-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, TerminalServerPort-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b9eea5c545613f05dbd828a9436175fab6bfc5a05ba2fe5f59588f78da913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512160"
---
# <a name="ivmguestosterminalserverport-property"></a>IVMGuestOS::TerminalServerPort-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Port, der von Remotedesktopdienste (früher als Terminaldienste bezeichnet) im Gastbetriebssystem verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Port zurück, der von Remotedesktopdienste im Gastbetriebssystem verwendet wird.



| Wert                                                                              | Bedeutung                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | Standardwert<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | Gültiger Bereich<br/>                        |
| <dl> <dt>0</dt> </dl>       | Ein gültiger Portwert ist nicht verfügbar.<br/> |



 

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Remotedesktopdienste ist im Gastbetriebssystem noch nicht initialisiert.<br/> |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                            | Der *tsPort-Parameter* ist **NULL.**<br/>                                           |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                                           |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Integrationskomponenten werden auf diesem virtuellen Computer nicht installiert.<br/>             |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                             |



## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist ungültig, es sei denn, die [**TerminalServicesInitialized-Eigenschaft**](ivmguestos-terminalservicesinitialized.md) ist **VARIANT \_ TRUE.**

Wenn die [**TerminalServicesInitialized-Eigenschaft**](ivmguestos-terminalservicesinitialized.md) aufgrund eines Verbindungsfehlers am Port **VARIANT \_ FALSE** ist, enthält der von der **TerminalServerPort-Eigenschaft** zurückgegebene Wert den Fehlerwert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                 |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                      |
| Idl<br/>                      | <dl> <dt>IVMGuestOS.idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

