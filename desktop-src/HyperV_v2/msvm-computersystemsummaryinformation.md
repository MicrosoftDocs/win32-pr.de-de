---
description: Enthält eine Informationszusammenfassung zum angegebenen virtuellen Computersystem.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 78ac2b89336a415bedd23e0ca4ecd6589abdefbf75a54900d716c78152d34d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531760"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>Msvm \_ ComputerSystemSummaryInformation-Klasse

Enthält eine Informationszusammenfassung zum angegebenen virtuellen Computersystem.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ComputerSystemSummaryInformation-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ComputerSystemSummaryInformation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**CIM \_ ComputerSystem-Objekt,**](cim-computersystem.md) das eine Instanz in der normalisierten Darstellung der verwalteten Ressource ist.

> [!Note]
>
> Datatype upgraded from [**Msvm \_ ComputerSystem**](msvm-computersystem.md) in Windows 10, Version 1703.

 

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ SummaryInformationBase**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("abhängig")
</dt> </dl>

Eine Instanz von [**Msvm \_ SummaryInformation,**](msvm-summaryinformation.md) die eine denormierte oder aggregierte Ansicht der verwalteten Ressource darstellt, die durch das [**Msvm \_ ComputerSystem**](msvm-computersystem.md) dargestellt wird, auf das von der Vorgängereigenschaft verwiesen wird.

> [!Note]
>
> Datatype updated from [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) in Windows 10, Version 1703.

 

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

[**CIM \_ ElementView**](cim-elementview.md)
</dt> </dl>

 

