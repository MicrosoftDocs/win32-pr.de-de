---
description: Stellt eine Zuordnung zwischen zwei Dienstzugriffspunkten (SAP) dar, bei der ein SAP von dem anderen abhängig ist, um einen Dienst zu nutzen oder eine Verbindung mit diesem herzustellen.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: CIM_SAPSAPDependency-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae8b1e45d1685204b15cf359f36cfced321fb75c099b7be76e0ece2ce3f836de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980860"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a>CIM_SAPSAPDependency-Klasse (Hyper-V-Verwaltung)

Stellt eine Zuordnung zwischen zwei Dienstzugriffspunkten (SAP) dar, bei der ein SAP von dem anderen abhängig ist, um einen Dienst zu nutzen oder eine Verbindung mit diesem herzustellen. Um beispielsweise auf einem Netzwerkdrucker zu drucken, müssen lokale Druckzugriffspunkte zugrunde liegende netzwerkbezogene SAPs verwenden, um die Druckanforderung zu senden.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Member

Die **\_ CIM SAPSAPDependency-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SAPSAPDependency-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein Verweis auf das erforderliche SAP.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein Verweis auf das abhängige SAP.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

