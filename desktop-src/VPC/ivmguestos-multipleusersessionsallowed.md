---
title: IVMGuestOS MultipleUserSessionsAllowed-Eigenschaft
description: Bestimmt, ob mehrere gleichzeitige Benutzersitzungen im Gastbetriebssystem zulässig sind.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- MultipleUserSessionsAllowed-Eigenschaft Virtueller PC
- MultipleUserSessionsAllowed-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, MultipleUserSessionsAllowed-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68075c13cfc65b79d992b849b310bd3c88b09f7901567baf249bff15496ede05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594073"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>IVMGuestOS::MultipleUserSessionsAllowed-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob mehrere gleichzeitige Benutzersitzungen im Gastbetriebssystem zulässig sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Eigenschaftswert

**VARIANT \_ TRUE,** wenn mehrere gleichzeitige Benutzersitzungen im Gastbetriebssystem zulässig sind, **andernfalls VARIANT \_ FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                       |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Remotedesktopdienste (ehemals Terminaldienste) wurde im Gastbetriebssystem noch nicht initialisiert.<br/> |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                            | Der *sessionStatus-Parameter* ist **NULL.**<br/>                                                                          |
| <dl> <dt>VM \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                                                                                 |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Integrationskomponenten werden auf diesem virtuellen Computer nicht installiert.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                   |



## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist nur gültig, wenn die [**TerminalServicesInitialized-Eigenschaft**](ivmguestos-terminalservicesinitialized.md) **VARIANT TRUE \_ ist.**

Für Windows Clientbetriebssysteme **ist MultipleUserSessionsAllowed** **variant \_ TRUE,** wenn schnelle Benutzerwechsel unterstützt werden. Für Windows Serverbetriebssysteme ist **MultipleUserSessionsAllowed** **variant \_ TRUE,** wenn Remotedesktopdienste (ehemals Terminaldienste) installiert und aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                 |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                      |
| Idl<br/>                      | <dl> <dt>IVMGuestOS.idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

