---
description: Dienst zum Erstellen, zerstören und Exportieren von Snapshot Collection von virtuellen Systemen.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348532"
---
# <a name="msvm_collectionsnapshotservice-class"></a>MSVM \_ collectionsnapshotservice-Klasse

Dienst zum Erstellen, zerstören und Exportieren von Snapshot Collection von virtuellen Systemen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **MSVM \_ collectionsnapshotservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM \_ collectionsnapshotservice** -Klasse verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Applysnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)                     | Wendet eine Momentaufnahme Sammlung auf die Sammlung des virtuellen Computer Systems an.<br/>                                                                                                                                        |
| [**Converttoreferencepoint**](msvm-collectionsnapshotservice-converttoreferencepoint.md) | Konvertiert eine vorhandene Auflistungs Momentaufnahme in eine Verweis Punkt Auflistung. Die Momentaufnahme Auflistung wird als Nebeneffekt gelöscht. Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.<br/>                      |
| [**CreateSnapshot**](msvm-collectionsnapshotservice-createsnapshot.md)                   | Erstellt eine Momentaufnahme einer virtuellen System Sammlung.<br/>                                                                                                                                                                 |
| [**Destroysnapshot**](msvm-collectionsnapshotservice-destroysnapshot.md)                 | Zerstört eine vorhandene Momentaufnahme der virtuellen System Sammlung. Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.<br/>                                                   |
| [**Export Momentaufnahme**](msvm-collectionsnapshotservice-exportsnapshot.md)                   | Exportiert eine Momentaufnahme Sammlung virtueller Computersysteme in eine Datei. Die Momentaufnahme Sammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




