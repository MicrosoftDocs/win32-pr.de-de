---
description: Die CIM DeviceAccessedByFile-Zuordnungsklasse gibt das logische Gerät an, auf das mithilfe der \_ REFERENZIERTEN CIM \_ DeviceFile-Klasse zugegriffen wird.
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: CIM_DeviceAccessedByFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24526d7743b1f4939f2240c751f7da2bfecfacfe13d2ddf3cbc7fdd73c1d260e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321640"
---
# <a name="cim_deviceaccessedbyfile-class"></a>\_CIM-Klasse "DeviceAccessedByFile"

Die **CIM \_ DeviceAccessedByFile-Zuordnungsklasse** gibt das logische Gerät an, auf das mithilfe der [**REFERENZIERTEN CIM \_ DeviceFile-Klasse zugegriffen**](cim-devicefile.md) wird.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a>Member

Die **\_ CIM-Klasse DeviceAccessedByFile** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Klasse DeviceAccessedByFile** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ DeviceFile**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorerst")
</dt> </dl>

Eine [**\_ CIM-Gerätedatei,**](cim-devicefile.md) die die Gerätedatei beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Eine [**CIM \_ LogicalDevice,**](cim-logicaldevice.md) die das Gerät beschreibt, auf das mithilfe der Gerätedatei zugegriffen wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Die **CIM \_ DeviceAccessedByFile-Klasse** wird von der [**\_ CIM-Abhängigkeit abgeleitet.**](cim-dependency.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

