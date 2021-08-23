---
title: IVMGuestOS OSMinorVersion-Eigenschaft (VPCCOMInterfaces.h)
description: Die Nebenversion des Gastbetriebssystems, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- OSMinorVersion-Eigenschaft Virtueller PC
- OSMinorVersion-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC , OSMinorVersion-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed509994c4105aeeb90f704b32f3e6bb10e9ad70791e607ebbae7db713ec60dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472544"
---
# <a name="ivmguestososminorversion-property"></a>IVMGuestOS::OSMinorVersion-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Nebenversion des Gastbetriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Nebenversion.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                        |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                            | Der Parameter ist **NULL.**<br/>                           |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ ausgeführt</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                               |
| <dl> <dt>VM \_ E \_ \_ ADDITIONSFUNKTION NICHT \_ \_ VERFÜGBAR</dt> <dt>0xA0040505</dt> </dl> | Integrationskomponenten werden auf dieser VM nicht installiert.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

