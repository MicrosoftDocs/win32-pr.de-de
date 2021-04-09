---
description: Bietet zusätzliche Informationen, die mit der exportreferencepoint-Methode der MSVM \_ virtualsystemreferencepointservice-Klasse verwendet werden können.
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
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050700"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a>MSVM \_ virtualsystemreferencepointexportsettingdata-Klasse

Bietet zusätzliche Informationen, die mit der [**exportreferencepoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) -Methode der [**MSVM \_ virtualsystemreferencepointservice**](msvm-virtualsystemreferencepointservice.md) -Klasse verwendet werden können.

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

Die **MSVM \_ virtualsystemreferencepointexportsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemreferencepointexportsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Basereferencepoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad des Basis Verweis Punkts, in Bezug auf den Export, der ausgeführt werden soll.

</dd> <dt>

**Diskstoexport**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

WMI-Instanz-IDs der Datenträger, für die Daten exportiert werden müssen.

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

 

 




