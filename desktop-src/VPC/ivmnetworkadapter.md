---
title: Ivmnetworkadapter-Schnittstelle (vpccominterfaces. h)
description: Dient als Schnittstelle für eine virtuelle Netzwerkschnittstellenkarte.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Ivmnetworkadapter Interface Virtual PC
- Virtueller Computer für ivmnetworkadapter Interface, beschrieben
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
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391957"
---
# <a name="ivmnetworkadapter-interface"></a>Ivmnetworkadapter-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Dient als Schnittstelle für eine virtuelle Netzwerkschnittstellenkarte (NIC). Es wird verwendet, um einzurichten, wie ein virtueller Computer vernetzt ist. Netzwerkschnittstellenkarten können mithilfe von [**ivmvirtualmachine:: addnetworkadapter**](ivmvirtualmachine-addnetworkadapter.md) und [**ivmvirtualmachine:: removenetworkadapter**](ivmvirtualmachine-removenetworkadapter.md)hinzugefügt und entfernt werden. Sie können auch ein **ivmnetworkadapter** -Objekt aus der [**ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md) -Sammlung abrufen, die von den Eigenschaften [**ivmvirtualmachine:: NetworkAdapters**](ivmvirtualmachine-networkadapters.md) oder [**ivmvirtualnetwork:: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) zurückgegeben wurde.

## <a name="members"></a>Member

Die **ivmnetworkadapter** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmnetworkadapter** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmnetworkadapter** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_id**](ivmnetworkadapter--id.md)                                          | Ruft den internen Bezeichner dieser Netzwerkschnittstelle ab.<br/>     |
| [**Attachanvirtualnetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Fügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk an.<br/> |
| [**Detachfromvirtualnetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Trennt die Netzwerkschnittstelle von Ihrem virtuellen Netzwerk.<br/>         |



 

### <a name="properties"></a>Eigenschaften

Die **ivmnetworkadapter** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                  | Zugriffstyp           | BESCHREIBUNG                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**Ethernetaddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Lesen/Schreiben<br/> | Die Ethernet-Adresse (Mac-Adresse) der Netzwerkschnittstelle.<br/>             |
| [**Isethernetaddressdynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob die Ethernet-Adresse dynamisch generiert wird.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Schreibgeschützt<br/>  | Der virtuelle Computer, der dieser Netzwerkschnittstelle zugeordnet ist.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Schreibgeschützt<br/>  | Das virtuelle Netzwerk, an das die Netzwerkschnittstelle angefügt wird.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Die standardethernet-Adresse für eine Netzwerkschnittstelle ist "00-00-00-00-00-00", die von den meisten Betriebssystemen als ungültige Ethernet-Adresse angesehen wird. Wenn [**isethernetaddressdynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) auf **false** festgelegt ist, muss [**ethernetaddress**](ivmnetworkadapter-ethernetaddress.md) mit einer gültigen Ethernet-Netzwerkadresse initialisiert werden.

In den folgenden Prozeduren wird erläutert, wie die **ivmnetworkadapter** -Schnittstelle verwendet wird.

**So fügen Sie eine virtuelle NIC an eine Host-NIC an**

-   Virtuelle (Guest) NICs sind nicht direkt an eine Host-NIC angefügt. Stattdessen wird die virtuelle NIC an ein virtuelles Netzwerk angefügt, das mit einer Host-NIC verbunden ist. Weitere Informationen zum Konfigurieren virtueller Netzwerke finden Sie unter [**ivmvirtualnetwork**](ivmvirtualnetwork.md). Verwenden Sie die [**attachdevirtualnetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) -Methode, um die virtuelle NIC an ein virtuelles Netzwerk anzufügen.

**So trennen Sie eine virtuelle NIC vom virtuellen Netzwerk**

-   Die Methode [**detachfromvirtualnetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) trennt die virtuelle NIC vom virtuellen Netzwerk. Nachdem diese Funktion aufgerufen wurde, gibt die [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) -Eigenschaft eine ungültige virtuelle Netzwerk-ID zurück.

**So entfernen Sie eine virtuelle NIC aus einer virtuellen Maschine, wenn Sie über das virtuelle NIC-Objekt verfügen**

1.  Holen Sie den virtuellen Computer, der der virtuellen NIC zugeordnet ist, mithilfe der [**virtualmachine**](ivmnetworkadapter-virtualmachine.md) -Eigenschaft ab.
2.  Verwenden Sie das aktuelle-Objekt als Parameter für die [**ivmvirtualmachine:: removenetworkadapter**](ivmvirtualmachine-removenetworkadapter.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.<br/>          |



 

