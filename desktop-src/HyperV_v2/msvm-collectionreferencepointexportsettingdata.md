---
description: Exportieren von Einstellungsdaten, die an die exportreferencepoint-Methode der MSVM \_ collectionreferencepointservice-Klasse übermittelt werden sollen.
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
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350078"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>MSVM \_ collectionreferencepointexportsettingdata-Klasse

Exportieren von Einstellungsdaten, die an die [**exportreferencepoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) -Methode der [**MSVM \_ collectionreferencepointservice**](msvm-collectionreferencepointservice.md) -Klasse übermittelt werden sollen.

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

Die **MSVM \_ collectionreferencepointexportsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ collectionreferencepointexportsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Basereferencepointcollection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Pfad zu einer [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) -Instanz, die die Basis-Verweis Punkt Auflistung darstellt, die für den differenziellen Export verwendet werden soll.

</dd> <dt>

**Virtualmachinestodiskstoexport**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **hypervembeddebug** ("MSVM \_ virtualmachinetodisks")
</dt> </dl>

Eine Liste der "VirtualMachines to diskstoexport"-Karteninformationen, für die Daten exportiert werden müssen.

</dd> </dl>

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

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




