---
title: Ivmharddisk-Schnittstelle (vpccominterfaces. h)
description: Ermöglicht den Zugriff auf ein Festplatten Abbild. Der Zugriff ist über die Eigenschaft "ivmharddiskconnection Harddisk" oder die Methode "ivmvirtualpc getharddisk" möglich.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Ivmharddisk Interface Virtual PC
- Virtueller Computer für ivmharddisk Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475039"
---
# <a name="ivmharddisk-interface"></a>Ivmharddisk-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ermöglicht den Zugriff auf ein Festplatten Abbild. Sie können über die [**ivmharddiskconnection:: Harddisk**](ivmharddiskconnection-harddisk.md) -Eigenschaft oder die [**ivmvirtualpc:: getharddisk**](ivmvirtualpc-getharddisk.md) -Methode darauf zugreifen.

## <a name="members"></a>Member

Die **ivmharddisk** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmharddisk** verfügt auch über die folgenden Typen von Mitgliedern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmharddisk** -Schnittstelle verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kompakt**](ivmharddisk-compact.md) | Komprimiert eine dynamisch erweiterbare virtuelle Festplatten Abbild.<br/>                                                                                        |
| [**Umgebaut**](ivmharddisk-convert.md) | Konvertiert eine virtuelle Festplatte entweder in eine dynamisch erweiterbare virtuelle Festplatte oder eine virtuelle Festplatte mit fester Größe.<br/>                            |
| [**Merge**](ivmharddisk-merge.md)     | Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträger Image zusammen.<br/>                                                                              |
| [**Mergeto**](ivmharddisk-mergeto.md) | Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Elementen (bis einschließlich der übergeordneten virtuellen Festplatte) einer neuen Festplatten Datei zusammen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ivmharddisk** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp           | BESCHREIBUNG                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Datei**](ivmharddisk-file.md)<br/>                           | Schreibgeschützt<br/>  | Der vollständige Pfadname der virtuellen Festplatten Datei.<br/>                                   |
| [**Hostfrediskspace**](ivmharddisk-hostfreediskspace.md)<br/> | Schreibgeschützt<br/>  | Die Menge des verbleibenden Speicherplatzes, der auf dem Host für die virtuelle Festplatte verfügbar ist.<br/> |
| [**Parent**](ivmharddisk-parent.md)<br/>                       | Lesen/Schreiben<br/> | Das übergeordnete Element der differenzierenden virtuellen Festplatte.<br/>                                   |
| [**Sizeingeguest**](ivmharddisk-sizeinguest.md)<br/>             | Schreibgeschützt<br/>  | Die Größe der virtuellen Festplatte im Gast Betriebssystem.<br/>                    |
| [**Sizeonhost**](ivmharddisk-sizeonhost.md)<br/>               | Schreibgeschützt<br/>  | Die Größe der virtuellen Festplatten Datei auf dem Host Computer.<br/>                        |
| [**type**](ivmharddisk-type.md)<br/>                           | Schreibgeschützt<br/>  | Der Typ der virtuellen Festplatte.<br/>                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



 

