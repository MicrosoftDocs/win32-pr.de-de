---
description: Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das den Auftrag erstellt hat.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: CIM_OwningJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351484"
---
# <a name="cim_owningjobelement-class"></a>CIM \_ owningjobelements-Klasse

Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das den Auftrag erstellt hat. Da ein Auftrag zwischen Systemen verschoben werden kann und das verwaltete Element möglicherweise nicht für die gesamte Dauer des Auftrags vorhanden ist, ist diese Zuordnung in einigen Fällen möglicherweise nicht möglich oder nur für einen Teil des Vorhandenseins des Auftrags vorhanden.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a>Member

Die **CIM \_ owningjobelements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ owningjobelements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Owdelta-Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Auftrag**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ein Verweis auf den Auftrag, der vom verwalteten Element erstellt wurde.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf das verwaltete Element, das den Auftrag erstellt hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

