---
title: Ivmharddiskconnection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Verbindung für eine Festplatte innerhalb des virtuellen Computers.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Virtuelle Computer der ivmharddiskconnection-Schnittstelle
- Virtueller Computer für die ivmharddiskconnection-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342023"
---
# <a name="ivmharddiskconnection-interface"></a>Ivmharddiskconnection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Verbindung für eine Festplatte innerhalb des virtuellen Computers. Ein **ivmharddiskconnection** -Objekt wird von der [**ivmvirtualmachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) -Methode zurückgegeben. Sie können auch ein **ivmharddiskconnection** -Objekt aus dem [**ivmharddiskconnectioncollection**](ivmharddiskconnectioncollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine:: harddiskconnections**](ivmvirtualmachine-harddiskconnections.md) -Eigenschaft zurückgegeben wird.

## <a name="members"></a>Member

Die **ivmharddiskconnection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmharddiskconnection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmharddiskconnection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**Setbuslokation**](ivmharddiskconnection-setbuslocation.md) | Legt den Busspeicherort fest, an den diese Festplatte angefügt ist.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ivmharddiskconnection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp          | BESCHREIBUNG                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**Busnummer**](ivmharddiskconnection-busnumber.md)<br/>       | Schreibgeschützt<br/> | Die Busnummer, an die das Laufwerks Bild angefügt wird.<br/>                   |
| [**Devicengegen ber**](ivmharddiskconnection-devicenumber.md)<br/> | Schreibgeschützt<br/> | Die Gerätenummer, an die das Laufwerks Image angefügt wird.<br/>                |
| [**Festplatten**](ivmharddiskconnection-harddisk.md)<br/>         | Schreibgeschützt<br/> | Ein Festplatten Objekt, das dieser Verbindung entspricht.<br/>                   |
| [**Undoharddisk**](ivmharddiskconnection-undoharddisk.md)<br/> | Schreibgeschützt<br/> | Ein Festplatten Objekt, das dem Rückgängig-Datenträger Image dieser Verbindung entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmharddiskconnection ist als aefa36a5-463a-46AE-9e6c-a1fb4e12e671 definiert.<br/>      |



 

