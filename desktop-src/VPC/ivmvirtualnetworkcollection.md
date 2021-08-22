---
title: IVMVirtualNetworkCollection-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert eine Auflistung von IVMVirtualNetwork-Objekten. Verwenden Sie zum Abrufen eines IVMVirtualNetworkCollection-Objekts die VirtualNetworks-Eigenschaft IVMVirtualPC.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- IVMVirtualNetworkCollection-Schnittstelle Virtueller PC
- IVMVirtualNetworkCollection-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32694b311482e58635ca28dc005fe68ab08495c15d251e176fb78266e7624e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592271"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>IVMVirtualNetworkCollection-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert eine Auflistung von [**IVMVirtualNetwork-Objekten.**](ivmvirtualnetwork.md) Um ein **IVMVirtualNetworkCollection-Objekt** abzurufen, verwenden Sie die [**IVMVirtualPC::VirtualNetworks-Eigenschaft.**](ivmvirtualpc-virtualnetworks.md)

## <a name="members"></a>Member

Die **IVMVirtualNetworkCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualNetworkCollection** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IVMVirtualNetworkCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | Beschreibung                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                                                  |
| [**Count**](ivmvirtualnetworkcollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der virtuellen Netzwerke in dieser Sammlung.<br/>                                                 |
| [**Element**](ivmvirtualnetworkcollection-item.md)<br/>          | Schreibgeschützt<br/> | Das [**IVMVirtualNetwork-Objekt,**](ivmvirtualnetwork.md) das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection ist als 8ed680be-4242-4b2a-a21c-1982d8b0f675 definiert.<br/> |



 

