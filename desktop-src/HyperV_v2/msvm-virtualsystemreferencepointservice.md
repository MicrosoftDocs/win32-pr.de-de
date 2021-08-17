---
description: Beschreibt einen Verweispunktdienst des virtuellen Systems.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f33ac35e9848b913978ef6fab91f60823e5c40e9a2bb652236b2ab902e4ea435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340160"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a>Msvm \_ VirtualSystemReferencePointService-Klasse

Beschreibt einen Verweispunktdienst des virtuellen Systems.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualSystemReferencePointService-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Msvm \_ VirtualSystemReferencePointService-Klasse** verfügt über diese Methoden.



| Methode                                                                                                       | Beschreibung                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | Erstellt einen Verweispunkt eines virtuellen Systems.<br/>            |
| [**DestroyReferencePoint**](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | Löscht den angegebenen Verweispunkt.<br/>                    |
| [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | Exportiert den Verweispunkt des virtuellen Systems.<br/>        |
| [**ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | Importiert Verweispunktmetadaten des virtuellen Systems.<br/>   |
| [**RemoveAssociatedData**](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | Entfernt das dem Verweispunkt zugeordnete Datenprotokoll.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Dienst**](cim-service.md)
</dt> </dl>

 

 




