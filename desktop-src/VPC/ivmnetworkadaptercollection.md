---
title: Ivmnetworkadaptercollection-Schnittstelle (vpccominterfaces. h)
description: Definiert eine Sammlung virtueller Netzwerkschnittstellenkarten. Zum Abrufen eines ivmnetworkadaptercollection-Objekts verwenden Sie die Eigenschaften "ivmvirtualmachine NetworkAdapters", "ivmvirtualnetwork Network Adapters" und "ivmvirtualpc unconnectednetworkadapters".
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Ivmnetworkadaptercollection-Schnittstelle virtueller PC
- Ivmnetworkadaptercollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040706"
---
# <a name="ivmnetworkadaptercollection-interface"></a>Ivmnetworkadaptercollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert eine Sammlung virtueller Netzwerkschnittstellenkarten. Zum Abrufen eines ivmnetworkadaptercollection-Objekts verwenden Sie die Eigenschaften [**ivmvirtualmachine:: NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**ivmvirtualnetwork:: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)und [**ivmvirtualpc:: unconnectednetworkadapters**](ivmvirtualpc-unconnectednetworkadapters.md) .

## <a name="members"></a>Member

Die **ivmnetworkadaptercollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmnetworkadaptercollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmnetworkadaptercollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmnetworkadaptercollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                                                  |
| [**Countdown**](ivmnetworkadaptercollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der Netzwerkschnittstellen in dieser Sammlung.<br/>                                               |
| [**Element**](ivmnetworkadaptercollection-item.md)<br/>          | Schreibgeschützt<br/> | Das [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ ivmnetworkadaptercollection ist als ebaeafe9-EBCD-47cf-866e-ad87d735e479 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmnetworkadapter**](ivmnetworkadapter.md)
</dt> <dt>

[**Ivmvirtualmachine:: NetworkAdapters**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**Ivmvirtualnetwork:: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**Ivmvirtualpc:: unconnectednetworkadapters**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

