---
title: IVMNetworkAdapter-Schnittstelle (VPCCOMInterfaces.h)
description: Dient als Schnittstelle zu einer virtuellen Netzwerkschnittstellenkarte.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- IVMNetworkAdapter-Schnittstelle Virtueller PC
- IVMNetworkAdapter-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73622161629f6d3746c153fb9e2df32ee120fd748defc60d0d02ef6ea4378b14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118843897"
---
# <a name="ivmnetworkadapter-interface"></a>IVMNetworkAdapter-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Dient als Schnittstelle zu einer virtuellen Netzwerkschnittstellenkarte (NIC). Sie wird verwendet, um einzurichten, wie ein virtueller Computer vernetzt wird. Netzwerkschnittstellenkarten können mithilfe von [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) und [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)hinzugefügt und entfernt werden. Sie können auch ein **IVMNetworkAdapter-Objekt** aus der [**IVMNetworkAdapterCollection-Auflistung**](ivmnetworkadaptercollection.md) abrufen, die von den Eigenschaften [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) oder [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) zurückgegeben wird.

## <a name="members"></a>Member

Die **IVMNetworkAdapter-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMNetworkAdapter** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMNetworkAdapter-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_Id**](ivmnetworkadapter--id.md)                                          | Ruft den internen Bezeichner dieser Netzwerkschnittstelle ab.<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Fügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk an.<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Trennt die Netzwerkschnittstelle von ihrem virtuellen Netzwerk.<br/>         |



 

### <a name="properties"></a>Eigenschaften

Die **IVMNetworkAdapter-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                  | Zugriffstyp           | BESCHREIBUNG                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Lesen/Schreiben<br/> | Die Ethernet-Adresse (MAC) der Netzwerkschnittstelle.<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob die Ethernet-Adresse dynamisch generiert wird.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Schreibgeschützt<br/>  | Der virtuelle Computer, der dieser Netzwerkschnittstelle zugeordnet ist.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Schreibgeschützt<br/>  | Das virtuelle Netzwerk, an das die Netzwerkschnittstelle angefügt ist.<br/>  |



 

## <a name="remarks"></a>Hinweise

Die Standard-Ethernet-Adresse für eine Netzwerkschnittstelle ist "00-00-00-00-00-00", was von den meisten Betriebssystemen als ungültige Ethernet-Adresse angesehen wird. Wenn [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) auf **FALSE** festgelegt ist, muss [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) mit einer gültigen Ethernet-Netzwerkadresse initialisiert werden.

In den folgenden Verfahren wird die Verwendung der **IVMNetworkAdapter-Schnittstelle** erläutert.

**So fügen Sie eine virtuelle NIC an eine Host-NIC an**

-   Virtuelle NICs (Gast-NICs) werden nicht direkt an eine Host-NIC angefügt. Stattdessen wird die virtuelle NIC an ein virtuelles Netzwerk angefügt, das an eine Host-NIC angefügt ist. Weitere Informationen zum Konfigurieren virtueller Netzwerke finden Sie unter [**IVMVirtualNetwork**](ivmvirtualnetwork.md). Um die virtuelle NIC an ein virtuelles Netzwerk anzufügen, verwenden Sie die [**AttachToVirtualNetwork-Methode.**](ivmnetworkadapter-attachtovirtualnetwork.md)

**So trennen Sie eine virtuelle NIC vom virtuellen Netzwerk**

-   Die [**DetachFromVirtualNetwork-Methode**](ivmnetworkadapter-detachfromvirtualnetwork.md) trennt die virtuelle NIC vom virtuellen Netzwerk. Nach dem Aufruf dieser Funktion gibt die [**VirtualNetwork-Eigenschaft**](ivmnetworkadapter-virtualnetwork.md) eine ungültige ID des virtuellen Netzwerks zurück.

**So entfernen Sie eine virtuelle NIC von einem virtuellen Computer, wenn Sie über das virtuelle NIC-Objekt verfügen**

1.  Abrufen des virtuellen Computers, der der virtuellen NIC zugeordnet ist, mithilfe der [**VirtualMachine-Eigenschaft.**](ivmnetworkadapter-virtualmachine.md)
2.  Verwenden Sie das aktuelle -Objekt als Parameter für die [**IVMVirtualMachine::RemoveNetworkAdapter-Methode.**](ivmvirtualmachine-removenetworkadapter.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter ist als e32e4165-22b8-4dc0-8d57-850171ae207a definiert.<br/>          |



 

