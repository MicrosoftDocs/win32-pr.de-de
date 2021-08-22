---
title: IVMParallelPort Name-Eigenschaft (VPCCOMInterfaces.h)
description: Name des parallelen Ports.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Name-Eigenschaft Virtueller PC
- Name-Eigenschaft Virtual PC , IVMParallelPort-Schnittstelle
- IVMParallelPort-Schnittstelle Virtueller PC , Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e4ce0ebf800329d40352adda9fa69d1233c8e72d0a5551a710b3c943b29fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510380"
---
# <a name="ivmparallelportname-property"></a>IVMParallelPort::Name-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Namen des parallelen Ports ab und legt den Namen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt den Namen des parallelen Ports fest (z. B. "LPT1").

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                              |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>                                 |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>      | Der -Parameter verweist auf einen ungültigen parallelen Port.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/>   |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort ist als 097beecb-0a02-474f-abd6-298b22293fc6 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

