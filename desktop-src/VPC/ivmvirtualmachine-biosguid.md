---
title: Ivmvirtualmachine biosguid-Eigenschaft (vpccominterfaces. h)
description: Die BIOS-GUID.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- Biosguid-Eigenschaft virtueller PC
- Biosguid-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, biosguid-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858863"
---
# <a name="ivmvirtualmachinebiosguid-property"></a>Ivmvirtualmachine:: biosguid-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die BIOS-GUID ab und legt Sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die BIOS-GUID an. Schließen Sie die hexadezimal Ziffern um die linke und die Rechte Klammer

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                               | Bedeutung                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                       |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                    | Der-Parameter ist **null**.<br/>                          |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>                 | Der-Parameter ist ungültig oder eine leere Zeichenfolge.<br/>   |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                       |
| <dl> <dt>VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_ </dt> <dt>0xa004020b</dt> gespeichert </dl> | Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                   |



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

 

