---
title: IVMNetworkAdapter EthernetAddress-Eigenschaft (VPCCOMInterfaces.h)
description: Ethernet-Adresse (MAC) der Netzwerkschnittstelle.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- EthernetAddress-Eigenschaft Virtueller PC
- EthernetAddress-Eigenschaft Virtueller PC, IVMNetworkAdapter-Schnittstelle
- IVMNetworkAdapter-Schnittstelle Virtueller PC, EthernetAddress-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3547bab24fdbaa50360a7198c020bb1dbc39b9efb9a1defad993a5be7a70fabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118844038"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>IVMNetworkAdapter::EthernetAddress (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Ethernet-Adresse (MAC) der Netzwerkschnittstelle ab und legt sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a>Eigenschaftswert

Die MAC-Adresse der virtuellen NIC. Sie sollte das Format "*XX* - *XX* - *XX* - *XX* - *XX* - *XX*" haben, wobei jedes *X* eine Hexadezimalziffer ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>                                                                                                   | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                              | Der Parameter ist **NULL.**<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>                           | Der -Parameter hat nicht das richtige Format.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>VM \_ E \_ CANT \_ SET DYNAMIC MAC ADDRESS \_ \_ \_ 0XA004070A</dt> <dt></dt> </dl> | Die Ethernet-Adresse für eine Netzwerkschnittstelle kann entweder dynamisch generiert oder vom Benutzer auf eine statische Adresse festgelegt werden. Diese Methode kann nicht aufgerufen werden, wenn die Adresse so festgelegt ist, dass sie dynamisch generiert wird. Die [**IsEthernetAddressDynamic-Eigenschaft**](ivmnetworkadapter-isethernetaddressdynamic.md) wird verwendet, um das Generierungsverhalten der Ethernet-Adresse zu ändern.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                      | Der virtuelle Computer wurde nicht gefunden. Dies kann auftreten, wenn der Computer entfernt wurde, nachdem das [**IVMNetworkAdapter-Objekt**](ivmnetworkadapter.md) erstellt wurde.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                      | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter ist als e32e4165-22b8-4dc0-8d57-850171ae207a definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

