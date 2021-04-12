---
title: Ivmguestos multipleusersessionsallowed (Eigenschaft)
description: Bestimmt, ob mehrere gleichzeitige Benutzersitzungen im Gast Betriebssystem zulässig sind.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Multipleusersessionsallowed-Eigenschaft virtueller PC
- Multipleusersessionsallowed-Eigenschaft virtueller PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, multipleusersessionsallowed (Eigenschaft)
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
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103970"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>Ivmguestos:: multipleusersessionsallowed (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Bestimmt, ob mehrere gleichzeitige Benutzersitzungen im Gast Betriebssystem zulässig sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Eigenschaftswert

**Variant \_ "True** ", wenn mehrere gleichzeitige Benutzersitzungen im Gast Betriebssystem zulässig sind, andernfalls " **\_ false** ".

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                       |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                                       | Remotedesktopdienste (früher als "Terminal Services" bezeichnet) wurde noch nicht im Gast Betriebssystem initialisiert.<br/> |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                            | Der *Sessionstatus* -Parameter ist **null**.<br/>                                                                          |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                                                                                 |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> " </dl> | Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.<br/>                                                   |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                   |



## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist nur gültig, wenn die [**terminalservicesinitialized**](ivmguestos-terminalservicesinitialized.md) -Eigenschaft **Variant \_ true** ist.

Bei Windows-Client Betriebssystemen ist **multipleusersessionsallowed** **Variant \_ true** , wenn die schnelle Benutzerumschaltung unterstützt wird. Bei Windows Server-Betriebssystemen ist **multipleusersessionsallowed** **Variant \_ true** , wenn Remotedesktopdienste (früher als "Terminal Services" bezeichnet) installiert und aktiviert ist.

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

 

