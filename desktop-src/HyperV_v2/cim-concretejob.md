---
description: Eine konkrete Version der CIM \_ Job-Klasse. Diese Klasse stellt eine generische instanziierbare Arbeitseinheit dar, die ausgeführt werden soll, z. B. ein Batch oder ein Druckauftrag.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a62ab2392ce2c069aa88ebb465f7028368f30bd5432cf96559c7eebe6edb8bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813161"
---
# <a name="cim_concretejob-class"></a>CIM \_ ConcreteJob-Klasse

Eine konkrete Version der [**CIM \_ Job-Klasse.**](cim-job.md) Diese Klasse stellt eine generische instanziierbare Arbeitseinheit dar, die ausgeführt werden soll, z. B. ein Batch oder ein Druckauftrag.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a>Member

Die **CIM \_ ConcreteJob-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ ConcreteJob-Klasse** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | Ruft Fehlerinformationen für den Betriebsstatus eines konkreten Auftrags ab.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Fordert die angegebene Zustandsänderung in einen konkreten Auftrag an.<br/>                    |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ConcreteJob-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifiziert eine Instanz dieser Klasse innerhalb des Bereichs des enthaltenden Namespaces eindeutig und nicht transparent.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespace sicherzustellen, sollte der Wert der **InstanceID-Eigenschaft** im folgenden Muster erstellt werden: *OrgID*:*LocalID*
>
> *OrgID* muss einen urheberrechtlich geschützten, markengeschützten oder anderweitig eindeutigen Namen enthalten, der sich im Besitz der Geschäftsentität befindet, die die **Instanz-ID** definiert, oder es muss sich um eine registrierte ID handeln, die von einer anerkannten globalen Autorität zugewiesen wird. Dieses Muster ähnelt der Struktur von Schemaklassennamen. Darüber hinaus muss der erste Doppelpunkt in **InstanceID** zwischen *orgID* und *LocalID* stehen, um eindeutig zu sein. Daher darf die *OrgID* keinen Doppelpunkt (":") enthalten.
>
> *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
>
> Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceID-Wert** nicht für alle **InstanceID-Eigenschaften** wiederverwendet wird, die von diesem Anbieter oder anderen Anbietern für diesen Namespace erstellt werden.
>
> Für definierte DMTF-Instanzen (Distributed Management Task Force) muss das Muster mit der *OrgID* verwendet werden, die auf CIM festgelegt ist.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Betriebszustand des Auftrags und der Übergang zwischen diesen Zuständen.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Neu** (2)


</dt> <dd>

der Auftrag wurde noch nie gestartet.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Ab** (3)


</dt> <dd>

Der Auftrag wechselt vom Status "Neu", "Angehalten" oder "Dienst" in den Status "Wird ausgeführt".

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Wird ausgeführt** (4)


</dt> <dd>

Der Auftrag wird ausgeführt.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Angehalten** (5)


</dt> <dd>

Der Auftrag wird beendet, kann aber nahtlos neu gestartet werden.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunterfahren** (6)


</dt> <dd>

Der Auftrag wechselt in den Zustand "Abgeschlossen", "Beendet" oder "Beendet".

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (7)


</dt> <dd>

Der Auftrag wurde normal abgeschlossen.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Beendet** (8)


</dt> <dd>

Der Auftrag wurde durch eine Beendigungsstatusänderungsanforderung beendet. Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können nur als neuer Auftrag neu gestartet werden (dies ist auftragsspezifisch).

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)


</dt> <dd>

Der Auftrag wurde durch eine Statusänderungsanforderung "Kill" beendet. Zugrunde liegende Prozesse wurden möglicherweise weiterhin ausgeführt, und möglicherweise ist eine Bereinigung erforderlich, um Ressourcen frei zu machen.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Ausnahme** (10)


</dt> <dd>

Der Auftrag befindet sich in einem ungewöhnlichen Zustand, der auf eine Fehlerbedingung hindeuten kann. Der tatsächliche Status wird möglicherweise über auftragsspezifische Objekte angezeigt.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (11)


</dt> <dd>

Der Auftrag befindet sich in einem anbieterspezifischen Zustand, der die Problemermittlung, -lösung oder beides unterstützt.

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Abfrage ausstehend** (12)


</dt> <dd>

Warten auf das Auflösen einer Abfrage durch einen Client.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (13..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Der benutzerfreundliche Name der Instanz. Darüber hinaus kann der benutzerfreundliche Name als Eigenschaft für eine Suche oder Abfrage verwendet werden.

> [!Note]  
> Der Name muss innerhalb des Namespace nicht eindeutig sein.

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Gibt an, wie lange ein abgeschlossener Auftrag beibehalten wird. Der Standardwert ist "00000000000500.000000:000" (fünf Minuten).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des Auftragszustands.

> [!Note]  
> Wenn sich der Status des Auftrags nicht geändert hat und diese Eigenschaft aufgefüllt wird, muss sie auf einen Intervallwert von 0 (null) festgelegt werden.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Auftrag**](cim-job.md)
</dt> </dl>

 

