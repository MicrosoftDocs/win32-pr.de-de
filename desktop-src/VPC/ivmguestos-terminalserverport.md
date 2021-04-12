---
title: Ivmguestos terminalserverport (Eigenschaft)
description: Port, der von Remotedesktopdienste im Gast Betriebssystem verwendet wird.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Terminalserverport-Eigenschaft virtueller PC
- Terminalserverport-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, terminalserverport (Eigenschaft)
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
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105818"
---
# <a name="ivmguestosterminalserverport-property"></a>Ivmguestos:: terminalserverport-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Port, der von Remotedesktopdienste (früher als "Terminal Services" bezeichnet) im Gast Betriebssystem verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Port zurück, der von Remotedesktopdienste im Gast Betriebssystem verwendet wird.



| Wert                                                                              | Bedeutung                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | Standardwert<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | Gültiger Bereich<br/>                        |
| <dl> <dt>0</dt> </dl>       | Ein gültiger Portwert ist nicht verfügbar.<br/> |



 

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                 |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                                       | Remotedesktopdienste wurde noch nicht im Gast Betriebssystem initialisiert.<br/> |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                            | Der *tsport* -Parameter ist **null**.<br/>                                           |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                                           |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> " </dl> | Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.<br/>             |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                             |



## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist nur gültig, wenn die [**terminalservicesinitialized**](ivmguestos-terminalservicesinitialized.md) -Eigenschaft **Variant \_ true** ist.

Wenn die [**terminalservicesinitialized**](ivmguestos-terminalservicesinitialized.md) -Eigenschaft aufgrund eines Verbindungsfehlers auf dem Port **Variant \_ false** ist, enthält der Wert, der von der Eigenschaft **terminalserverport** zurückgegeben wird, den Fehlerwert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                 |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                      |
| IDL<br/>                      | <dl> <dt>Ivmguestos. idl</dt> </dl> |
| IID<br/>                      | IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmguestos**](ivmguestos.md)
</dt> </dl>

 

