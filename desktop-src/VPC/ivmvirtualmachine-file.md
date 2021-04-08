---
title: Ivmvirtualmachine-Datei Eigenschaft (vpccominterfaces. h)
description: Ruft den voll qualifizierten Pfad der VMC-Datei für die Konfiguration der virtuellen Maschine ab.
ms.assetid: fc215068-e908-417c-bd68-214539a0a14e
keywords:
- Datei Eigenschaft virtueller PC
- Datei Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, File-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.File
- IVMVirtualMachine.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ac3bc68d167a7057d76adc1ce84a29291b7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742049"
---
# <a name="ivmvirtualmachinefile-property"></a>Ivmvirtualmachine:: File (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den voll qualifizierten Pfad der VMC-Datei für die Konfiguration der virtuellen Maschine ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_File(
  [out, retval] BSTR *virtualMachineXMLFile
);
```



## <a name="property-value"></a>Eigenschaftswert

Der voll qualifizierte Name der \* VMC-Datei, in der diese Konfiguration der virtuellen Maschine beschrieben wird.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



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

 

