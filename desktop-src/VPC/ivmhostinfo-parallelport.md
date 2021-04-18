---
title: Ivmhostinfo Parallelport-Eigenschaft (vpccominterfaces. h)
description: Ruft den parallelen Host Anschluss ab, der an den Gast angefügt werden kann.
ms.assetid: 4c9486b8-ab66-4874-b467-a7a0ab7934f1
keywords:
- Parallelport-Eigenschaft virtueller PC
- Parallelport-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, Parallelport (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.ParallelPort
- IVMHostInfo.get_ParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0a2050ff505f5ed7a54cf3857ea28661d4d3d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517348"
---
# <a name="ivmhostinfoparallelport-property"></a>Ivmhostinfo::P arallelport-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den parallelen Host Anschluss ab, der an den Gast angefügt werden kann.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ParallelPort(
  [out, retval] BSTR *vmParallelPort
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des parallelen Anschlusses.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmhostinfo**](ivmhostinfo.md)
</dt> </dl>

 

