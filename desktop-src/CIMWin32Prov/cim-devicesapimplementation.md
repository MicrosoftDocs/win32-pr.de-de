---
description: Die CIM DeviceSAPImplementation-Klasse stellt eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner \_ Implementierung dar.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: CIM_DeviceSAPImplementation -Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1643441d24e465ff7311daae52e4bc7773b556c7719ec7a93c35ff478740fd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321610"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a>CIM_DeviceSAPImplementation -Klasse (CIMWin32-WMI-Anbieter)

Die **CIM \_ DeviceSAPImplementation-Klasse** stellt eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung dar. Wenn viele logische Geräte einem SAP zugeordnet sind, werden die Elemente zusammen verwendet, um den Zugriffspunkt zu ermöglichen. Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des SAP-Objekts.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ DeviceSAPImplementation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Klasse DeviceSAPImplementation** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorerst")
</dt> </dl>

Ein [**CIM \_ LogicalDevice,**](cim-logicaldevice.md) das das logische Gerät beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**CIM \_ ServiceAccessPoint,**](cim-serviceaccesspoint.md) der den dienstzugriffspunkt beschreibt, der mit dem logischen Gerät implementiert wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Die **CIM \_ DeviceSAPImplementation-Klasse** wird von der [**CIM-Abhängigkeit \_ abgeleitet.**](cim-dependency.md)

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

 

