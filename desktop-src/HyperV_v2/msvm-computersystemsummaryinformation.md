---
description: Enthält eine Zusammenfassung der Informationen zum angegebenen virtuellen Computersystem.
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
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862652"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>MSVM \_ computersystemsummaryinformation-Klasse

Enthält eine Zusammenfassung der Informationen zum angegebenen virtuellen Computersystem.

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

Die **MSVM \_ computersystemsummaryinformation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ computersystemsummaryinformation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt, bei dem es sich um eine Instanz in der normalisierten Darstellung der verwalteten Ressource handelt.

> [!Note]
>
> DataType, aktualisiert von [**MSVM \_ Computersystem**](msvm-computersystem.md) in Windows 10, Version 1703.

 

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ summaryinformationbase**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Eine Instanz von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , die eine entnormalisierte oder aggregierte Ansicht der verwalteten Ressource darstellt, die durch das [**MSVM \_ Computersystem**](msvm-computersystem.md) dargestellt wird, auf das von der Vorgänger Eigenschaft verwiesen wird.

> [!Note]
>
> DataType wurde aus [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) in Windows 10, Version 1703, aktualisiert.

 

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

[**CIM- \_ Element Ansicht**](cim-elementview.md)
</dt> </dl>

 

