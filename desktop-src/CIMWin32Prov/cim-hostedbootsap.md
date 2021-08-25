---
description: Die CIM \_ HostedBootSAP-Klasse definiert das hostende unitäre Computersystem für eine CIM \_ BootSAP-Klasse.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: CIM_HostedBootSAP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69bad7de1a680054f93a9cb63596fff30538b31c02019e08ac58f643a0d81c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923590"
---
# <a name="cim_hostedbootsap-class"></a>CIM \_ HostedBootSAP-Klasse

Die **CIM \_ HostedBootSAP-Klasse** definiert das hostende unitäre Computersystem für eine [**CIM \_ BootSAP-Klasse.**](cim-bootsap.md) Da diese Beziehung von [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)untergliedert ist, erbt sie das Bereichs-/Benennungsschema, das für [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)definiert ist, wobei ein Zugriffspunkt auf sein Hostingsystem zurückgreift. In diesem Fall muss **CIM \_ BootSAP** auf die hostende [**CIM \_ UnitaryComputerSystem-Klasse**](cim-unitarycomputersystem.md) zurückstellen.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ HostedBootSAP-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ HostedBootSAP-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ UnitaryComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**CIM \_ UnitaryComputerSystem, das**](cim-unitarycomputersystem.md) das unitäre Computersystem beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ BootSAP**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**\_ CIM-BootSAP,**](cim-bootsap.md) der den auf dem unitären Computersystem gehosteten Start-SAP beschreibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ HostedBootSAP-Klasse** wird von [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)abgeleitet.

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

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

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)
</dt> </dl>

 

