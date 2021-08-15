---
title: IVMVirtualMachine Memory-Eigenschaft (VPCCOMInterfaces.h)
description: Menge des physischen Arbeitsspeichers auf dem virtuellen Computer in Megabyte.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Memory-Eigenschaft Virtueller PC
- Memory-Eigenschaft Virtual PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, Memory-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a828dde1804e546c97fe7cd2c161fc45366d416ba0e44900816c7bbee4b1ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344664"
---
# <a name="ivmvirtualmachinememory-property"></a>IVMVirtualMachine::Memory -Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Menge des physischen Arbeitsspeichers auf dem virtuellen Computer in Megabyte ab und legt sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die Menge des physischen Arbeitsspeichers in Megabyte an.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                         | Bedeutung                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>                  |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>              | Der Parameter ist **NULL.**<br/>                     |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>           | Der -Parameter ist ungültig oder liegt nicht im gültigen Bereich.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>                  |
| <dl> <dt>VM \_ E \_ PREF \_ NOT \_ FOUND</dt> <dt>0xA0040300</dt> </dl> | Die Einstellung wurde nicht gefunden.<br/>                  |
| <dl> <dt>VM \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | Der virtuelle Computer wird ausgeführt oder gespeichert.<br/>       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/>              |



## <a name="remarks"></a>Hinweise

Die Menge des physischen Arbeitsspeichers auf einem virtuellen Computer muss mindestens 4 MB betragen. Die Obergrenze für den Arbeitsspeicher hängt von der Hostkonfiguration ab, kann aber mindestens 3.712 MB betragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

