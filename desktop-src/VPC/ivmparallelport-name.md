---
title: Ivmparallelport-Namenseigenschaft (vpccominterfaces. h)
description: Der Name des parallelen Anschlusses.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Name-Eigenschaft virtueller PC
- Name-Eigenschaft Virtual PC, ivmparallelport-Schnittstelle
- Ivmparallelport Interface Virtual PC, Name-Eigenschaft
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
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102803"
---
# <a name="ivmparallelportname-property"></a>Ivmparallelport:: Name-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Namen des parallelen Ports ab und legt ihn fest.

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

Legt den Namen des parallelen Anschlusses fest (z. b. "LPT1").

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                              |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>                                 |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>      | Der-Parameter verweist auf einen ungültigen parallelen Port.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/>   |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmparallelport ist als 097beecb-0a02-474b-abd6-298b22293fc6 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmparallelport**](ivmparallelport.md)
</dt> </dl>

 

