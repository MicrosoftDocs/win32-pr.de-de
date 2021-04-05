---
title: Ivmvirtualmachine chassisassettag-Eigenschaft (vpccominterfaces. h)
description: Chassis-Bestands Kennzeichen.
ms.assetid: 469816a8-3078-4960-a5e1-79d65b5fc8fc
keywords:
- Chassisassettag-Eigenschaft virtueller PC
- Chassisassettag-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, chassisassettag (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisAssetTag
- IVMVirtualMachine.get_ChassisAssetTag
- IVMVirtualMachine.put_ChassisAssetTag
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d02f71907121354c4d937436366548d41f9944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859024"
---
# <a name="ivmvirtualmachinechassisassettag-property"></a>Ivmvirtualmachine:: chassisassettag (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das Chassis-assettag ab und legt es fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ChassisAssetTag(
  [in]          BSTR chassisAssetTag
);

HRESULT get_ChassisAssetTag(
  [out, retval] BSTR *chassisAssetTag
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt das Chassis-Asset-Tag an.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                               | Bedeutung                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                                               |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                    | Der-Parameter ist **null**.<br/>                                                  |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>                 | Der-Parameter ist größer als 32 Zeichen, eine leere Zeichenfolge oder ungültig.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                                               |
| <dl> <dt>VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_ </dt> <dt>0xa004020b</dt> gespeichert </dl> | Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".<br/>                         |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                           |



## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält keine gültigen Informationen, bis der virtuelle Computer zum ersten Mal gestartet wurde. Eine leere Zeichenfolge wird zurückgegeben, wenn Sie vor dem ersten Start gelesen wird.

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

 

