---
title: Ivmvirtualmachine-Maus Eigenschaft (vpccominterfaces. h)
description: Ruft das Mausgerät für den virtuellen Computer ab.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Mouseproperty Virtual PC
- Mouseproperty Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, Maus Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342665"
---
# <a name="ivmvirtualmachinemouse-property"></a>Ivmvirtualmachine:: Mouse-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das Mausgerät für den virtuellen Computer ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**ivmmouse**](ivmmouse.md) -Objekt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                         | Bedeutung                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>              | Der-Parameter ist **null**.<br/>          |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>       |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl> | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

