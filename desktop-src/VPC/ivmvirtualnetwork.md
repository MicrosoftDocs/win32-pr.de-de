---
title: Ivmvirtualnetwork-Schnittstelle (vpccominterfaces. h)
description: Definiert ein virtuelles Netzwerk.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Ivmvirtualnetwork Interface Virtual PC
- Ivmvirtualnetwork Interface Virtual PC, beschrieben
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
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346531"
---
# <a name="ivmvirtualnetwork-interface"></a>Ivmvirtualnetwork-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert ein virtuelles Netzwerk. **Ivmvirtualnetwork** -Objekte werden von der [**ivmvirtualpc**](ivmvirtualpc.md) -Methode " [**findvirtualnetwork**](ivmvirtualpc-findvirtualnetwork.md)" zurückgegeben. Sie können auch ein **ivmvirtualnetwork** -Objekt aus dem [**ivmvirtualnetworkcollection**](ivmvirtualnetworkcollection.md) -Objekt abrufen, das von der [**ivmvirtualpc:: virtualnetworks**](ivmvirtualpc-virtualnetworks.md) -Eigenschaft zurückgegeben wird.

Ein virtuelles Netzwerk besteht aus einem virtuellen Switch, der das gesamte interne Routing ausführt, und mehreren Verbindungen, die an den virtuellen Switch angeschlossen sind. Dabei kann es sich um eine echte externe Host Verbindung, ein "internes Netzwerk" oder ein frei gegebenes Netzwerk (Network Network, NAT) handeln.

## <a name="members"></a>Member

Die **ivmvirtualnetwork** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmvirtualnetwork** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmvirtualnetwork** -Schnittstelle verfügt über diese Methoden.



| Methode                                | BESCHREIBUNG                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_id**](ivmvirtualnetwork--id.md) | Ruft den internen Bezeichner des virtuellen Netzwerks ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ivmvirtualnetwork** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp          | BESCHREIBUNG                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**Host Adapter "**](ivmvirtualnetwork-hostadapter.md)<br/>         | Schreibgeschützt<br/> | Der Name des Adapters, mit dem das virtuelle Netzwerk verbunden ist.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Schreibgeschützt<br/> | Bestimmt, ob die virtuelle Netzwerk Instanz drahtlos ist oder nicht.<br/> |
| [**Name**](ivmvirtualnetwork-name.md)<br/>                       | Schreibgeschützt<br/> | Der eindeutige Name der virtuellen Netzwerk Instanz.<br/>                    |
| [**Netzwerkadapter**](ivmvirtualnetwork-networkadapters.md)<br/> | Schreibgeschützt<br/> | Eine Aufzähl Bare Auflistung von NICs, die an das virtuelle Netzwerk angefügt sind.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualnetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.<br/>          |



 

