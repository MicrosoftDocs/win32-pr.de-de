---
description: Ordnet dem Verwaltungsdienst eine Instanz des virtuellen Computers zu, der den Zustand steuert.
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
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130000"
---
# <a name="msvm_serviceaffectselement-class"></a>MSVM \_ serviceaffectselements-Klasse

Ordnet dem Verwaltungsdienst eine Instanz des virtuellen Computers zu, der den Zustand steuert.

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

Die **MSVM \_ serviceaffectselements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ serviceaffectselements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Affectedelta-Element**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt.

</dd> <dt>

**Affectingelement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf den Dienst, der den virtuellen Computer steuert. Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt.

</dd> <dt>

**Elementeffects**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ des Steuer Elements an, das die Zuordnung darstellt. Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt und ist immer auf den folgenden Wert festgelegt.



| Wert                                                                        | Bedeutung            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Verwaltet<br/> |



 

</dd> <dt>

**Otherelementeffect-Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Details für den Typ der Zuordnung an der entsprechenden Array Position in der **Element beeinflusst** das Eigenschafts Array. Diese Informationen sind erforderlich, wenn **Element Affekte** auf 1 (Sonstiges) festgelegt ist. Diese Eigenschaft wird von [**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ serviceaffectselements** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ serviceaffectselements**](cim-serviceaffectselement.md)
</dt> <dt>

[**CIM \_ serviceaffectselements**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

