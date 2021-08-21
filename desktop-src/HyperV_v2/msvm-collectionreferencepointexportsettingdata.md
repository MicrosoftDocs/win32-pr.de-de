---
description: Exportieren Sie Einstellungsdaten, die an die ExportReferencePoint-Methode der Msvm \_ CollectionReferencePointService-Klasse übergeben werden sollen.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Msvm_CollectionReferencePointExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b8b160f16a71e25eca4afa445fd05fd1faba58c82c6ba6e08afd25bbc9ba41b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149243"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>Msvm \_ CollectionReferencePointExportSettingData-Klasse

Exportieren Sie Einstellungsdaten, die an die [**ExportReferencePoint-Methode**](msvm-collectionreferencepointservice-exportreferencepoint.md) der [**Msvm \_ CollectionReferencePointService-Klasse**](msvm-collectionreferencepointservice.md) übergeben werden sollen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a>Member

Die **Msvm \_ CollectionReferencePointExportSettingData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ CollectionReferencePointExportSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BaseReferencePointCollection**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Pfad zu einer [**Msvm \_ ReferencePointCollection-Instanz,**](msvm-referencepointcollection.md) die die Basisverweispunktauflistung darstellt, die für den differenziellen Export verwendet werden soll.

</dd> <dt>

**VirtualMachinesToDisksToExport**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **HyperVEmbeddedInstance** ("Msvm \_ VirtualMachineToDisks")
</dt> </dl>

Liste der Zuordnungsinformationen zu "VirtualMachines To DisksToExport", für die Daten exportiert werden müssen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




