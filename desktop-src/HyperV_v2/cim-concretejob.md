---
description: Eine konkrete Version der CIM- \_ Auftrags Klasse. Diese Klasse stellt eine generische instanziier Bare Arbeitseinheit dar, die ausgeführt werden soll, z. b. einen Batch oder einen Druckauftrag.
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
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356819"
---
# <a name="cim_concretejob-class"></a>CIM- \_ Klasse "concretejob"

Eine konkrete Version der [**CIM- \_ Auftrags**](cim-job.md) Klasse. Diese Klasse stellt eine generische instanziier Bare Arbeitseinheit dar, die ausgeführt werden soll, z. b. einen Batch oder einen Druckauftrag.

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

Die CIM-Klasse " **\_ concretejob** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die CIM-Klasse " **\_ concretejob** " verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | Hiermit werden Fehlerinformationen für den Betriebsstatus eines konkreten Auftrags abgerufen.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Fordert die angegebene Zustandsänderung an einen konkreten Auftrag an.<br/>                    |



 

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ concretejob** " verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Eindeutig und verdeckt identifiziert eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*
>
> *OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId** definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird. Dieses Muster ähnelt der Struktur von Schema Klassennamen. Um die Eindeutigkeit sicherzustellen, muss der erste Doppelpunkt in **InstanceId** zwischen der *OrgId* und der *Lok-* ID liegen. Daher darf die *OrgId* keinen Doppelpunkt (': ') enthalten.
>
> *LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
>
> Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.
>
> Für von DMTF (verteilte Management Task Force) definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Betriebsstatus des Auftrags und der Übergang zwischen diesen Zuständen.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Neu** (2)


</dt> <dd>

der Auftrag wurde nie gestartet.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)


</dt> <dd>

Der Auftrag wechselt von den Zuständen "neu", "angehalten" oder "Dienst" in den Zustand "wird ausgeführt".

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (4)


</dt> <dd>

Der Auftrag wird ausgeführt.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (5** )


</dt> <dd>

Der Auftrag wurde angehalten, kann jedoch nahtlos neu gestartet werden.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (6)


</dt> <dd>

Der Auftrag wechselt in den Zustand "abgeschlossen", "beendet" oder "abgebrochen".

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (7)


</dt> <dd>

Der Auftrag wurde normal abgeschlossen.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Beendet** (8)


</dt> <dd>

Der Auftrag wurde mit dem Status "beenden" beendet Change Request. Der Auftrag und alle zugrunde liegenden Prozesse werden beendet und können (Dies ist Auftrags spezifisch) nur als neuer Auftrag neu gestartet werden.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>Abgeb **Rochen (9** )


</dt> <dd>

Der Auftrag wurde mit dem Status "Kill" beendet Change Request. Die zugrunde liegenden Prozesse wurden möglicherweise noch ausgeführt, und die Bereinigung ist möglicherweise erforderlich, um Ressourcen freizugeben.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Ausnahme** (10)


</dt> <dd>

Der Auftrag befindet sich in einem nicht ordnungsgemäßen Zustand, der möglicherweise auf eine Fehlerbedingung hinweist. Der tatsächliche Status wird möglicherweise auch in auftragsspezifischen Objekten angezeigt.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (11)


</dt> <dd>

Der Auftrag befindet sich in einem herstellerspezifischen Zustand, der die Problem Ermittlung, Lösung oder beides unterstützt.

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Abfrage ausstehend** (12)


</dt> <dd>

Es wird darauf gewartet, dass ein Client eine Abfrage auflöst.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (13.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name")
</dt> </dl>

Der benutzerfreundliche Name der-Instanz. Außerdem kann der benutzerfreundliche Name als Eigenschaft für eine Suche oder Abfrage verwendet werden.

> [!Note]  
> Der Name muss innerhalb des Namespace nicht eindeutig sein.

 

</dd> <dt>

**Timebeforeremoval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Gibt an, wie lange ein abgeschlossener Auftrag beibehalten wird. Der Standardwert ist "00000000000500.000000:000" (fünf Minuten).

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des Auftrags Zustands.

> [!Note]  
> Wenn der Status des Auftrags nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 (null) festgelegt werden.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Auftrag**](cim-job.md)
</dt> </dl>

 

