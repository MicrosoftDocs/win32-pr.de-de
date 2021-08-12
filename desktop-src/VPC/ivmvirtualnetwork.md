---
title: IVMVirtualNetwork-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert ein virtuelles Netzwerk.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- IVMVirtualNetwork-Schnittstelle Virtueller PC
- IVMVirtualNetwork-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9caf5accb0add3354953d09e74a0893e2392deee7720b7a2cba0136b3f4b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592585"
---
# <a name="ivmvirtualnetwork-interface"></a>IVMVirtualNetwork-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert ein virtuelles Netzwerk. **IVMVirtualNetwork-Objekte** werden von der [**IVMVirtualPC-Methode**](ivmvirtualpc.md) [**FindVirtualNetwork zurückgegeben.**](ivmvirtualpc-findvirtualnetwork.md) Sie können auch ein **IVMVirtualNetwork-Objekt** aus dem [**IVMVirtualNetworkCollection-Objekt**](ivmvirtualnetworkcollection.md) abrufen, das von der [**IVMVirtualPC::VirtualNetworks-Eigenschaft zurückgegeben**](ivmvirtualpc-virtualnetworks.md) wird.

Ein virtuelles Netzwerk besteht aus einem virtuellen Switch, der das interne Routing ausführt, und mehreren Verbindungen, die mit dem virtuellen Switch verbunden sind. Diese Verbindungen können eine echte externe Hostverbindung, ein "internes Netzwerk" oder ein freigegebenes Netzwerk (Shared Networking, NAT) sein.

## <a name="members"></a>Member

Die **IVMVirtualNetwork-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualNetwork** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMVirtualNetwork-Schnittstelle** verfügt über diese Methoden.



| Methode                                | BESCHREIBUNG                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_Id**](ivmvirtualnetwork--id.md) | Ruft den internen Bezeichner des virtuellen Netzwerks ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IVMVirtualNetwork-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp          | BESCHREIBUNG                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**Hostadapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | Schreibgeschützt<br/> | Der Name des Adapters, mit dem das virtuelle Netzwerk verbunden ist.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Schreibgeschützt<br/> | Bestimmt, ob die Instanz des virtuellen Netzwerks drahtlos ist oder nicht.<br/> |
| [**Namen**](ivmvirtualnetwork-name.md)<br/>                       | Schreibgeschützt<br/> | Der eindeutige Name der Instanz des virtuellen Netzwerks.<br/>                    |
| [**NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)<br/> | Schreibgeschützt<br/> | Eine aufzählbare Sammlung von NICs, die an das virtuelle Netzwerk angefügt sind.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.<br/>          |



 

