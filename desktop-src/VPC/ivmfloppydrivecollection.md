---
title: Ivmfloppydrivecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert eine Sammlung von Diskettenlaufwerken innerhalb des virtuellen Computers.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Ivmfloppydrivecollection Interface Virtual PC
- Ivmfloppydrivecollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392202"
---
# <a name="ivmfloppydrivecollection-interface"></a>Ivmfloppydrivecollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert eine Sammlung von Diskettenlaufwerken innerhalb des virtuellen Computers. Zum Abrufen eines **ivmfloppydrivecollection** -Objekts verwenden Sie die [**ivmvirtualmachine:: floppydrives**](ivmvirtualmachine-floppydrives.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmfloppydrivecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmfloppydrivecollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmfloppydrivecollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                          | Zugriffstyp          | BESCHREIBUNG                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmfloppydrivecollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                |
| [**Countdown**](ivmfloppydrivecollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der Diskettenlaufwerke in dieser Auflistung.<br/>                  |
| [**Element**](ivmfloppydrivecollection-item.md)<br/>          | Schreibgeschützt<br/> | Das Disketten Laufwerks Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmfloppydrivecollection ist als 8ba70a25-s698-4ee5-85ce-3cc93a925516 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmfloppydrive**](ivmfloppydrive.md)
</dt> <dt>

[**Ivmvirtualmachine:: floppydrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

