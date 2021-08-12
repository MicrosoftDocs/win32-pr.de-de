---
title: IVMGuestOS CanShutdown-Eigenschaft (VPCCOMInterfaces.h)
description: Gibt an, ob das Gastbetriebssystem sauber heruntergefahren werden kann.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- CanShutdown-Eigenschaft Virtueller PC
- CanShutdown-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, CanShutdown-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29396178a376fb9649b2a953c4086c4c1460744cd1b4268645dba9877125cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594752"
---
# <a name="ivmguestoscanshutdown-property"></a>IVMGuestOS::CanShutdown-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt an, ob das Gastbetriebssystem sauber heruntergefahren werden kann (erfordert Integrationskomponenten).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a>Eigenschaftswert

**VARIANT \_ TRUE,** wenn das Betriebssystem den Vorgang zum Herunterfahren unterstützt, **andernfalls VARIANT \_ FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>           |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer ist nicht aktiviert.<br/>   |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>              |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Der virtuelle Computer wurde nicht gefunden.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

