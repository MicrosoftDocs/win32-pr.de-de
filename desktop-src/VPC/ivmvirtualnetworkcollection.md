---
title: Ivmvirtualnetworkcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert eine Auflistung von ivmvirtualnetwork-Objekten. Verwenden Sie zum Abrufen eines ivmvirtualnetworkcollection-Objekts die ivmvirtualpc-virtualnetworks-Eigenschaft.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Ivmvirtualnetworkcollection-Schnittstelle virtueller PC
- Ivmvirtualnetworkcollection Interface Virtual PC, beschrieben
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
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743081"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Ivmvirtualnetworkcollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert eine Auflistung von [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekten. Zum Abrufen eines **ivmvirtualnetworkcollection** -Objekts verwenden Sie die [**ivmvirtualpc:: virtualnetworks**](ivmvirtualpc-virtualnetworks.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmvirtualnetworkcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmvirtualnetworkcollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmvirtualnetworkcollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmvirtualnetworkcollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                                                  |
| [**Countdown**](ivmvirtualnetworkcollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der virtuellen Netzwerke in dieser Sammlung.<br/>                                                 |
| [**Element**](ivmvirtualnetworkcollection-item.md)<br/>          | Schreibgeschützt<br/> | Das [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ ivmvirtualnetworkcollection ist als 8ed680be-4242-4b2a-A21C-1982d8b0f. definiert.<br/> |



 

