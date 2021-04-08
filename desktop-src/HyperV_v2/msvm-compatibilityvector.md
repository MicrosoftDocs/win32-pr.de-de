---
description: Verweist auf die Kompatibilitätsinformationen für einen virtuellen Computer (VM) (bei Ausführen auf einem VM-Computersystem) oder einen Host (bei der auf einem Host Computersystem ausgeführt).
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
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866412"
---
# <a name="msvm_compatibilityvector-class"></a>MSVM \_ compatibilityvector-Klasse

Verweist auf die Kompatibilitätsinformationen für einen virtuellen Computer (VM) (bei Ausführen auf einem VM-Computersystem) oder einen Host (bei der auf einem Host Computersystem ausgeführt).

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

Die **MSVM \_ compatibilityvector** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ compatibilityvector** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Compareoperation**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bezeichnet die Vergleichsoperation, bei der nur dann true zurückgegeben wird, wenn zwei Vektoren kompatibel sind. Die Daten des virtuellen Computers befinden sich auf der linken Seite des Vergleichs, und die Daten des Hosts befinden sich auf der rechten Seite.

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**Gleich** (0)


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

**Superset** (1)


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

**Mehrfach** (8)


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

**Divisible** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Compatibilityinfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die tatsächlichen Kompatibilitäts Attributdaten, die für den Vergleich verwendet werden.

</dd> <dt>

**Vectorid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert einen Kompatibilitäts Vektor, der ein bestimmtes Attribut darstellt. Diese Eigenschaft wird verwendet, um die entsprechenden Vektoren zwischen einem Host und einem virtuellen Computer abzugleichen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**getsystemcompatibilityvectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse gibt ein Array von **MSVM- \_ compatibilityvector** -Instanzen für den Host (wenn Sie auf dem Host ausgeführt werden) oder einen virtuellen Computer (wenn auf dem virtuellen Computer ausgeführt wird) zurück. Jeder **MSVM \_ compatibilityvector** -Eintrag in der Liste beschreibt einen Kompatibilitäts Attribut Vektor. Damit ein virtueller Computer mit einem Host kompatibel ist, müssen alle zugehörigen Kompatibilitäts Attribute mit den Attributen des Hosts kompatibel sein.

Jeder **MSVM \_ compatibilityvector** -Eintrag verfügt über folgende Eigenschaften:

<dl> <dt>

**Vectorid**
</dt> <dd>

Identifiziert den Kompatibilitäts Vektor eindeutig. Diese wird verwendet, um die Vektoren für den Vergleich zwischen einem Host und einem virtuellen Computer abzugleichen.

</dd> <dt>

**Compareoperation**
</dt> <dd>

Identifiziert den Vergleichs Vorgang, der bestimmt, ob die Vektoren kompatibel sind.

</dd> <dt>

**Compatibilityinfo**
</dt> <dd>

Enthält das tatsächliche Kompatibilitäts Attribut. Dabei handelt es sich um die Attribut Nutzlast (z. b. Prozessor Funktions Maske, Größe von Cache Zeilen Leerung usw.).

</dd> </dl>

Der Satz von Vorgängen, der für **compareoperation** definiert ist, umfasst nur grundlegende ganzzahlige Vergleiche und bitweise Logik. Dies ermöglicht, dass der tatsächliche Inhalt von **compatibilityinfo** nicht transparent bleibt. Der Satz von Vorgängen umfasst Folgendes:



| Compareoperation | BESCHREIBUNG                                      | Pseudo Code Vergleich                |
|------------------|--------------------------------------------------|--------------------------------------|
| Vmccequal        | Vmattr muss auf "" gehostet werden.                       | If (vmattr = = gehostet)              |
| Vmccsuperset     | Vmattr muss eine übergeordnete Gruppe von "sestattr" sein.            | If ((vmattr & "blau) = =" " |
| Vmccsubset       | Vmattr muss eine Teilmenge von "sestattr" sein.              | If ((vmattr-&-Eigenschaft) = = vmattr)   |
| Vmccdisjointset  | Bei vmattr muss es sich um eine zusammenhängende Gruppe von "hustattr" handeln      | If ((vmattr-&-Eigenschaft) = = 0)        |
| Vmccgreater      | Vmattr muss höher sein als "".             | If (vmattr >-Eigenschaft)            |
| Vmccgreaterequal | Vmattr muss größer als oder gleich "hustattr" sein. | If (vmattr >= gehostet)           |
| Vmccless         | Vmattr muss kleiner sein als "".                | If (vmattr <-Eigenschaft)            |
| Vmcclessequal    | "Vmattr" muss kleiner oder gleich "hustattr" sein.    | If (vmattr <= gehostet)           |
| Vmccmultiple     | Vmattr muss ein Vielfaches von "".            | If ((vmattr% hustattr) = = 0)        |
| Vmccdivisor      | Vmattr muss ein Divisor von "Host-r" sein.             | If (("", "% vmattr") = = 0)        |



 

SCVMM muss diese Schritte ausführen, um zu bestimmen, ob ein virtueller Computer mit einem Host kompatibel ist.

**So bestimmen Sie, ob ein virtueller Computer mit einem Host kompatibel ist**

1.  Iterieren Sie alle **MSVM \_ compatibilityvector** -Elemente für den virtuellen Computer.
2.  Verwenden Sie für jedes **MSVM \_ compatibilityvector** -Element den in **compareoperation** angegebenen Kompatibilitäts Vorgang, um den Hardware Kompatibilitäts Vektor des virtuellen Computers mit dem entsprechenden Kompatibilitäts Vektor für den Host zu vergleichen.
3.  Wenn alle **MSVM \_ compatibilityvector** -Elemente aus dem virtuellen Computer als kompatibel eingestuft werden, ist der virtuelle Computer mit dem Host kompatibel (aus Sicht des Prozessor Features).

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

[**Getsystemcompatibilityvectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




