---
description: Ordnet dem Verwaltungsdienst, der seinen Zustand steuert, eine Instanz eines virtuellen Computers zu.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db9ab0ff0aa3eab6f0268f7e85cb5f4efd0e7d2624c7e97a95abb3dd3b414ab2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582280"
---
# <a name="msvm_serviceaffectselement-class"></a>Msvm \_ ServiceAffectsElement-Klasse

Ordnet dem Verwaltungsdienst, der seinen Zustand steuert, eine Instanz eines virtuellen Computers zu.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Member

Die **Msvm \_ ServiceAffectsElement-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ServiceAffectsElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ ServiceAffectsElement geerbt.**](/previous-versions//cc136907(v=vs.85))

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den Dienst, der den virtuellen Computer steuert. Diese Eigenschaft wird von [**CIM \_ ServiceAffectsElement geerbt.**](/previous-versions//cc136907(v=vs.85))

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ des Steuerelements an, das die Zuordnung darstellt. Diese Eigenschaft wird von [**CIM \_ ServiceAffectsElement geerbt**](/previous-versions//cc136907(v=vs.85))und immer auf den folgenden Wert festgelegt.



| Wert                                                                        | Bedeutung            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Verwaltet<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Details für den Zuordnungstyp an der entsprechenden Arrayposition im **ElementAffects-Eigenschaftenarray.** Diese Informationen sind erforderlich, **wenn ElementAffects** auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft wird von [**CIM \_ ServiceAffectsElement geerbt**](/previous-versions//cc136907(v=vs.85))und immer auf NULL **festgelegt.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ServiceAffectsElement-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ServiceAffectsElement**](cim-serviceaffectselement.md)
</dt> <dt>

[**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

