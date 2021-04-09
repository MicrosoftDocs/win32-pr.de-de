---
title: Ivmnetworkadapter-ethernetaddress-Eigenschaft (vpccominterfaces. h)
description: Ethernet-Adresse (Mac-Adresse) der Netzwerkschnittstelle.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Ethernetaddress-Eigenschaft virtueller PC
- Ethernetaddress-Eigenschaft Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, ethernetaddress-Eigenschaft
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
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739760"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>Ivmnetworkadapter:: ethernetaddress-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Ethernet-Adresse (Mac-Adresse) der Netzwerkschnittstelle ab und legt Sie fest.

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

Die Mac-Adresse der virtuellen NIC. Er sollte das Format "*xx* XX XX XX XX -  -  -  -  - *xx*" aufweisen, wobei jedes *X* eine hexadezimale Ziffer ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>                                                                                                   | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                              | Der-Parameter ist **null**.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>                           | Der-Parameter weist nicht das richtige Format auf.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>VM \_ E \_ cant \_ \_ dynamische \_ Mac- \_ Adresse</dt> <dt>0xa004070a</dt> festlegen </dl> | Die Ethernet-Adresse für eine Netzwerkschnittstelle kann entweder dynamisch generiert werden, oder Sie kann vom Benutzer auf eine statische Adresse festgelegt werden. Diese Methode kann nicht aufgerufen werden, wenn die Adresse für die dynamische Generierung festgelegt ist. Die [**isethernetaddressdynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) -Eigenschaft wird verwendet, um das Generierungs Verhalten der Ethernet-Adresse zu ändern.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>                      | Der virtuelle Computer wurde nicht gefunden. Dies kann vorkommen, wenn der Computer entfernt wurde, nachdem das [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt erstellt wurde.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                      | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmnetworkadapter**](ivmnetworkadapter.md)
</dt> </dl>

 

