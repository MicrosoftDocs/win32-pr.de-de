---
description: Die CIM \_ servicesapdepen-Klasse stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der angibt, dass der referenzierte SAP vom Dienst verwendet wird, um seine Funktionalität bereitzustellen.
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: CIM_ServiceSAPDependency-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126662"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a>CIM_ServiceSAPDependency-Klasse (cimwin32-WMI-Anbieter)

Die **CIM \_ servicesapdepen-Klasse** stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der angibt, dass der referenzierte SAP vom Dienst verwendet wird, um seine Funktionalität bereitzustellen. Start Dienste können z. b. BIOS-Datenträger Dienste (Interrupts) aufrufen, um zu funktionieren.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ servicesapdepenpklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ servicesapdepenpklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ serviceaccesspoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der den erforderlichen Dienst Zugriffspunkt beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Dienst**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein [**CIM- \_ Dienst**](cim-service.md) , der den Dienst beschreibt, der von einem zugrunde liegenden SAP abhängig ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert.

Die **CIM- \_ servicesapdepenpklasse** wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

