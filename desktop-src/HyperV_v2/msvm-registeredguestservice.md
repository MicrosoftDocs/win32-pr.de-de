---
description: Stellt eine Zuordnung zwischen einer Instanz von MSVM \_ guestserviceinterfacecomponent und einer Instanz von MSVM \_ guestservice dar, die einen Dienst darstellt, der im Gast Betriebssystem ausgeführt wird.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Msvm_RegisteredGuestService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756894"
---
# <a name="msvm_registeredguestservice-class"></a>MSVM \_ registeredguestservice-Klasse

Stellt eine Zuordnung zwischen einer Instanz von [**MSVM \_ guestserviceinterfacecomponent**](msvm-guestserviceinterfacecomponent.md) und einer Instanz von [**MSVM \_ guestservice**](msvm-guestservice.md)dar, die einen Dienst darstellt, der im Gast Betriebssystem ausgeführt wird. Diese Klasse wird von der [**CIM- \_ Abhängigkeits**](/windows/desktop/CIMWin32Prov/cim-dependency) Klasse abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ registeredguestservice** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ registeredguestservice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ guestserviceinterfacecomponent**](msvm-guestserviceinterfacecomponent.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")
</dt> </dl>

Verweis auf die Komponente der Gast Dienst Schnittstelle in dieser Zuordnung.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ guestservice**](msvm-guestservice.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")
</dt> </dl>

Verweis auf den registrierten Gast Dienst, der von der **Vorgänger** Eigenschaft abhängt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

