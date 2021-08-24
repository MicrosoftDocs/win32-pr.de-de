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
ms.openlocfilehash: 8ea0e4371246f71d125295730c19de75c59eafb08a4c081699b6b40575f27a99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694660"
---
# <a name="cim_owningjobelement-class"></a>CIM \_ OwningJobElement-Klasse

Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das den Auftrag erstellt hat. Da ein Auftrag zwischen Systemen wechseln kann und das verwaltete Element während der gesamten Dauer des Auftrags möglicherweise nicht vorhanden ist, ist diese Zuordnung in einigen Fällen möglicherweise nicht möglich oder nur für einen Teil des Auftragsbestands vorhanden.

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

Die **CIM \_ OwningJobElement-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ OwningJobElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**OwnedElement**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Auftrag**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ein Verweis auf den Auftrag, der vom verwalteten Element erstellt wurde.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
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
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

