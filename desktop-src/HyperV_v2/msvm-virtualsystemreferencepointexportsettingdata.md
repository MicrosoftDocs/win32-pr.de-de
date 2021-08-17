---
description: Stellt zusätzliche Informationen zur Verwendung mit der ExportReferencePoint-Methode der Msvm \_ VirtualSystemReferencePointService-Klasse zur Verfügung.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Msvm_VirtualSystemReferencePointExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b3fc743d8431d76582553979bb25e1269df970d70187c65c2bddd1014834c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147943"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a>Msvm \_ VirtualSystemReferencePointExportSettingData-Klasse

Stellt zusätzliche Informationen zur Verwendung mit der [**ExportReferencePoint-Methode**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) der [**Msvm \_ VirtualSystemReferencePointService-Klasse**](msvm-virtualsystemreferencepointservice.md) zur Verfügung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualSystemReferencePointExportSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualSystemReferencePointExportSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BaseReferencePoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Pfad des Basisverweispunkts in Bezug auf den Export, der ausgeführt werden soll.

</dd> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

WMI-Instanz-IDs der Datenträger, für die Daten exportiert werden müssen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




