---
description: Die \_ CIM-Zuordnung AssociatedZusammenhängende gibt an, wann Lüfter oder andere Kühlgeräte spezifisch für ein Gerät sind (im Gegensatz zur Bereitstellung von Gehäuse- oder Gehäusekühlung).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: CIM_AssociatedCooling-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71f9c129a7883e5594affeefab8de9c20cf30ff092c5ce315471dbf5bc0a316a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119218940"
---
# <a name="cim_associatedcooling-class"></a>CIM \_ AssociatedClass

Die **\_ CIM-Zuordnung AssociatedZusammenhängende** gibt an, wann Lüfter oder andere Kühlgeräte spezifisch für ein Gerät sind (im Gegensatz zur Bereitstellung von Gehäuse- oder Gehäusekühlung).

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ AssociatedMembering-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Diese Eigenschaften sind in der **\_ CIM-Klasse Associated Csving** enthalten.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CoolingDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Eine [**CIM \_ LogicalDevice,**](cim-logicaldevice.md) die das Kühlgerät beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**CIM \_ LogicalDevice,**](cim-logicaldevice.md) der auf das logische Gerät verweist, das gerade ausgesperrt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ AssociatedClassing-Klasse** wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)abgeleitet.

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

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

