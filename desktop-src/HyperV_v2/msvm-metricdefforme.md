---
description: Definiert die Zuordnung zwischen einer Msvm \_ BaseMetricDefinition und einem CIM \_ ManagedElement, um Metriken für letzteres zu definieren. Die Metrikdefinition wird vom ManagedElement kontextabhängig, weshalb die Definition vom -Element abhängig ist.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Msvm_MetricDefForME-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c6da093c5f902657c51285e124593e0bf44a9be0bf32ed87a55d3349cbfba92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521600"
---
# <a name="msvm_metricdefforme-class"></a>Msvm \_ MetricDefForME-Klasse

Definiert die Zuordnung zwischen einer [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) und einem [**CIM \_ ManagedElement,**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) um Metriken für letzteres zu definieren. Die Metrikdefinition wird vom ManagedElement kontextabhängig, weshalb die Definition vom -Element abhängig ist.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a>Member

Die **Msvm \_ MetricDefForME-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ MetricDefForME-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine Instanz der [**CIM \_ ManagedElement-Klasse,**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) die das verwaltete Element darstellt, auf das Metriken des von **Dependent** definierten Typs angewendet werden können. Diese Eigenschaft wird von [**\_ CIM-Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine Instanz der [**CIM \_ BaseMetricDefinition-Klasse,**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) die die Metrikdefinition darstellt, die der **Vorgänger** darauf anwenden kann. Diese Eigenschaft wird von [**\_ CIM-Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**MetricCollectionEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die von **Dependent** definierte Metrik für **den** Vorgänger erfasst wird. Dies ist einer der folgenden Werte.



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Aktiviert**</dt> <dt>2</dt> </dl>                                         | Die Metrik wird erfasst.<br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>3</dt> </dl>                                     | Die Metrik wird nicht erfasst.<br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Reserviert**</dt> <dt>4</dt> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <dt>**PartiallyEnabled**</dt> <dt>32768</dt> </dl> | Die Metrik wird für einige, aber nicht für alle Geräte erfasst.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

