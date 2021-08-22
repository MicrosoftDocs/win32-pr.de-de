---
description: Verweist auf die Kompatibilitätsinformationen für einen virtuellen Computer (VM) (wenn er auf einem VM-Computersystem ausgeführt wird) oder einen Host (bei Ausführung auf einem Hostcomputersystem).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 976e6b7bd9bf69e483b987da4d8055ffc102e89c67ed83bab6aa09c4e586b1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531840"
---
# <a name="msvm_compatibilityvector-class"></a>Msvm \_ CompatibilityVector-Klasse

Verweist auf die Kompatibilitätsinformationen für einen virtuellen Computer (VM) (wenn er auf einem VM-Computersystem ausgeführt wird) oder einen Host (bei Ausführung auf einem Hostcomputersystem).

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a>Member

Die **Msvm \_ CompatibilityVector-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ CompatibilityVector-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CompareOperation**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Vergleichsvorgang, der "true" zurück gibt, wenn und nur dann, wenn zwei Vektoren kompatibel sind. Die Daten des virtuellen Computers werden auf der linken Seite des Vergleichs angezeigt, und die Daten des Hosts sind auf der rechten Seite.

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**Gleich** (0)


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

**Obermenge** (1)


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

**Teilmenge** (2)


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

**Disjoint** (3)


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

**GreaterThan** (4)


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

**GreaterThanOrEqual** (5)


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

**LessThan** (6)


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

**LessThanOrEqual** (7)


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

**Multiple** (8)


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

**Divisible** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**CompatibilityInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die tatsächlichen Kompatibilitätsattributdaten, die für den Vergleich verwendet werden.

</dd> <dt>

**VectorId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert einen Kompatibilitätsvektor, der ein bestimmtes Attribut darstellt. Diese Eigenschaft wird verwendet, um entsprechende Vektoren zwischen einem Host und einem virtuellen Computer zu verwenden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**GetSystemCompatibilityVectors-Methode**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) der [**Msvm \_ VirtualSystemMigrationService-Klasse**](msvm-virtualsystemmigrationservice.md) gibt ein Array von **Msvm \_ CompatibilityVector-Instanzen** für den Host (bei Ausführung auf dem Host) oder einen virtuellen Computer (bei Ausführung auf dem virtuellen Computer) zurück. Jeder **Msvm \_ CompatibilityVector-Eintrag** in der Liste beschreibt einen Kompatibilitätsattributvektor. Damit ein virtueller Computer mit einem Host kompatibel ist, müssen alle seine Kompatibilitätsattribute mit den Attributen des Hosts kompatibel sein.

Jeder **Msvm \_ CompatibilityVector-Eintrag** verfügt über die folgenden Eigenschaften:

<dl> <dt>

**VectorId**
</dt> <dd>

Identifiziert den Kompatibilitätsvektor eindeutig. Dies wird verwendet, um die Vektoren für den Vergleich zwischen einem Host und einem virtuellen Computer zu vergleichen.

</dd> <dt>

**CompareOperation**
</dt> <dd>

Identifiziert den Vergleichsvorgang, der bestimmt, ob die Vektoren kompatibel sind.

</dd> <dt>

**CompatibilityInfo**
</dt> <dd>

Enthält das tatsächliche Kompatibilitätsattribut. Dies ist effektiv die Attributnutzlast (z. B. Prozessorfunktionsmaske, Cachezeilenleergröße usw.).

</dd> </dl>

Die für **CompareOperation** definierten Vorgänge umfassen lediglich einen einfachen Ganzzahlvergleich und eine bitweise Logik. Dadurch bleibt der tatsächliche Inhalt von **CompatibilityInfo** undurchsichtig. Der Satz von Vorgängen umfasst Folgendes:



| CompareOperation | Beschreibung                                      | Pseudocodevergleich                |
|------------------|--------------------------------------------------|--------------------------------------|
| VmCcEqual        | VmAttr muss HostAttr gleich sein.                       | If (VmAttr == HostAttr)              |
| VmCcSuperSet     | VmAttr muss eine Obermenge von HostAttr sein.            | If ((VmAttr & HostAttr) == HostAttr) |
| VmCcSubSet       | VmAttr muss eine Teilmenge von HostAttr sein.              | If ((VmAttr & HostAttr) == VmAttr)   |
| VmCcDisjointSet  | "VmAttr" muss nicht mit HostAttr entiert sein.      | If ((VmAttr & HostAttr) == 0)        |
| VmCcGreater      | VmAttr muss größer als HostAttr sein.             | If (VmAttr > HostAttr)            |
| VmCcGreaterEqual | VmAttr muss größer oder gleich HostAttr sein. | If (VmAttr >= HostAttr)           |
| VmCcLess         | VmAttr muss kleiner als HostAttr sein                | If (VmAttr < HostAttr)            |
| VmCcLessEqual    | VmAttr muss kleiner oder gleich HostAttr sein.    | If (VmAttr <= HostAttr)           |
| VmCcMultiple     | VmAttr muss ein Vielfaches von HostAttr sein.            | If ((VmAttr % HostAttr) == 0)        |
| VmCcDivisor      | VmAttr muss ein Divisor von HostAttr sein.             | If ((HostAttr % VmAttr) == 0)        |



 

SCVMM muss diese Schritte ausführen, um zu bestimmen, ob eine VM mit einem Host kompatibel ist.

**So bestimmen Sie, ob eine VM mit einem Host kompatibel ist**

1.  Iterieren Sie alle **Msvm \_ CompatibilityVector-Elemente** für den virtuellen Computer.
2.  Verwenden Sie **für jedes Msvm \_ CompatibilityVector-Element** den in **CompareOperation** angegebenen Kompatibilitätsvorgang, um den Hardwarekompatibilitätsvektor des virtuellen Computers mit dem entsprechenden Kompatibilitätsvektor für den Host zu vergleichen.
3.  Wenn alle **Msvm \_ CompatibilityVector-Elemente** des virtuellen Computers als kompatibel angesehen werden, ist die VM mit dem Host kompatibel (aus Der Perspektive der Prozessorfunktion).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




