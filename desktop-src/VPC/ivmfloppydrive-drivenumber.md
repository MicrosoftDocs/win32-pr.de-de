---
title: Ivmfloppydrive-drivenenumber-Eigenschaft (vpccominterfaces. h)
description: Ruft den NULL basierten Index des Controllers ab, an den das Diskettenlaufwerk angefügt ist.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- Drivenumschlag-Eigenschaft virtueller PC
- Drivenumschlag-Eigenschaft Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, drivenumschlag-Eigenschaft
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858970"
---
# <a name="ivmfloppydrivedrivenumber-property"></a>Ivmfloppydrive::D rivenumber-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den NULL basierten Index des Controllers ab, an den das Diskettenlaufwerk angefügt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a>Eigenschaftswert

Der null basierte Index des Controllers.

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
| IID<br/>                      | IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmfloppydrive**](ivmfloppydrive.md)
</dt> </dl>

 

