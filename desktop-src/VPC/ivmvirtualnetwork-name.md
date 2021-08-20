---
title: IVMVirtualNetwork Name-Eigenschaft (VPCCOMInterfaces.h)
description: Eindeutiger Name der Instanz des virtuellen Netzwerks.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Name-Eigenschaft Virtueller PC
- Name-Eigenschaft Virtual PC, IVMVirtualNetwork-Schnittstelle
- IVMVirtualNetwork-Schnittstelle Virtueller PC, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79cd7ba9e06c7e3ed8c2788d749d5a010b1299bfd4c635570ff161197e70c22f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122645"
---
# <a name="ivmvirtualnetworkname-property"></a>IVMVirtualNetwork::Name (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den eindeutigen Namen der Instanz des virtuellen Netzwerks ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a>Eigenschaftswert

Den Namen des virtuellen Netzwerks.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                                |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>                                                   |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten, oder die Instanz des virtuellen Netzwerks ist unbekannt.<br/> |



## <a name="remarks"></a>Hinweise

Bei Namen virtueller Netzwerke wird die Groß-/Kleinschreibung nicht beachtet, z. B. verweisen "MyNetwork" und "mynetwork" auf dasselbe virtuelle Netzwerk.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

