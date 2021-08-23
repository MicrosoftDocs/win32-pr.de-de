---
title: IVMGuestOS TerminalServicesInitialized-Eigenschaft (VPCCOMInterfaces.h)
description: Status der Remotedesktopdienste im Gastbetriebssystem.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- TerminalServicesInitialisierte Eigenschaft Virtueller PC
- TerminalServicesInitialisierte Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, TerminalServicesInitialisierte Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595ae6028bea1984a320a699d204e4d3c23c1ca44e021cbbd994bbc5b832655a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512150"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a>IVMGuestOS::TerminalServicesInitialized-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Status von Remotedesktopdienste (früher als Terminaldienste bezeichnet) im Gastbetriebssystem ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Initialisierungsstatus.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang war erfolgreich, und Remotedesktopdienste wurde initialisiert. Der zurückgegebene Eigenschaftswert gibt an, ob Remotedesktopdienste im Gastbetriebssystem verfügbar ist.<br/> |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Die Integrationskomponentenfunktion wird ausgeführt, aber Remotedesktopdienste ist noch nicht initialisiert.<br/>                                                                                               |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                            | Der Parameter ist **NULL.**<br/>                                                                                                                                                                       |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.<br/>                                                                                                                                     |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Die Integrationskomponentenfunktion wird im Gastbetriebssystem nicht ausgeführt.<br/>                                                                                                                 |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

