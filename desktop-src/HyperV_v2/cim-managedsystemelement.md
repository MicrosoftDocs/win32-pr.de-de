---
description: CIM \_ ManagedSystemElement ist die Basisklasse für die System Element Hierarchie. Jede Komponente eines Systems kann durch diese Klasse oder deren Unterklassen möglicherweise dargestellt werden.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: CIM_ManagedSystemElement-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216771"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a>CIM_ManagedSystemElement-Klasse (Hyper-V-Verwaltung)

**CIM \_ ManagedSystemElement** ist die Basisklasse für die System Element Hierarchie. Jede Komponente eines Systems kann durch diese Klasse oder deren Unterklassen möglicherweise dargestellt werden.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a>Member

Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Communicationstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit diesem Element zu kommunizieren. Ein **null** -Wert gibt an, dass die Instrumentierung diese Eigenschaft nicht unterstützt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

**Nicht verfügbar** (1)


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

**Kommunikation OK** (2)


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

**Verlorene Kommunikation** (3)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (0X8000..)


</dt> <dd></dd> </dl>

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**Primarystatus**","**CIM \_ ManagedSystemElement**.**Healthstate**")
</dt> </dl>

Gibt zusätzliche Status Details an, die die **primarystatus** -Eigenschaft ergänzen. Ein **null** -Wert gibt an, dass die Instrumentierung diese Eigenschaft nicht unterstützt.

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

**Nicht verfügbar** (0)


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

**Keine zusätzlichen Informationen** (1)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** (2)


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

**Vorhersagefehler** (3)


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

**Nicht BEHEB barer Fehler** (4)


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

**Unterstützende Entität in Error** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (0X8000..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktuellen Zustand des Elements an. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise die Integrität seiner unter Komponenten.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (5)


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

Heruntergestuft **/Warnung** (10)


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

**Kleinerer Fehler** (15)


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

**Größerer Fehler** (20)


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

**Kritischer Fehler** (25)


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

**Nicht BEHEB barer Fehler** (30)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts weist nicht darauf hin, dass das Objekt nicht installiert ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Die Bezeichnung, mit der das-Objekt bekannt ist. Bei einer Unterklasse kann die **Name** -Eigenschaft als Schlüsseleigenschaft überschrieben werden.

</dd> <dt>

**Operatingstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**Enabledstate**")
</dt> </dl>

Gibt den aktuellen Betriebszustand des Elements an. Diese Eigenschaft kann verwendet werden, um weitere Details zum Wert der **enabledstate** -Eigenschaft bereitzustellen. Ein **null** -Wert gibt an, dass die Instrumentierung diese Eigenschaft nicht unterstützt.

"Unknown" gibt an

"None" gibt an, dass

Deten

Fahren

Hindern

"Beendet" und "abgebrochen" sind ähnlich, obwohl das erste

"Ruhende" gibt an, dass

"Abgeschlossen" zeigt an, dass t

Nen

"Immigration"

"Migration"

"Herunterfahren"

"In Test"

Übergang

"In Dienst"

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Die-Implementierung ist in der Regel in der Lage, diese Eigenschaft zurückzugeben, kann dies jedoch zu diesem Zeitpunkt nicht tun.

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)


</dt> <dd>

Die Implementierung (Provider) ist in der Lage, einen Wert für diese Eigenschaft zurückzugeben, aber nicht jemals für diese bestimmte Hardware/Software. die Eigenschaft wird nicht absichtlich verwendet, da Sie keine aussagekräftigen Informationen hinzufügt (wie im Fall einer Eigenschaft, die zum Hinzufügen zusätzlicher Informationen zu einer anderen Eigenschaft vorgesehen ist).

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)


</dt> <dd>

Beschreibt ein Element, das konfiguriert, gewartet, bereinigt oder anderweitig verwaltet wird.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)


</dt> <dd>

Beschreibt ein Element, das initialisiert wird.

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )


</dt> <dd>

Beschreibt ein Element, das zu einem ordnungsgemäßen Ende gebracht wird.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)


</dt> <dd>

Ein sauberer und ordnungsgemäßes Ende ist aufgetreten.

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)


</dt> <dd>

Es ist ein abruptes Beenden aufgetreten, bei dem der Status und die Konfiguration des Elements möglicherweise aktualisiert werden müssen.

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)


</dt> <dd>

Das Element ist inaktiv oder inaktiv.

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)


</dt> <dd>

Das Element hat seinen Vorgang abgeschlossen. Dieser Wert sollte entweder mit "OK", "Fehler" oder "heruntergestuft" in "primarystatus" kombiniert werden, damit ein Client ermitteln kann, ob der vollständige Vorgang mit "OK (bestanden)" abgeschlossen, mit "Fehler" (Fehler) abgeschlossen oder mit "heruntergestuft" abgeschlossen wurde (der Vorgang wurde beendet, aber nicht abgeschlossen oder ein Fehler nicht gemeldet).

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)


</dt> <dd>

Das Element wird zwischen Host Elementen verschoben.

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)


</dt> <dd>

Das Element wird vom Host Element entfernt.

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)


</dt> <dd>

Das Element wird zu einem neuen Host Element verschoben.

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)


</dt> <dd>

Beschreibt ein Element, das zu einem abrupten beenden geführt wird.

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)


</dt> <dd>

Das-Element führt Testfunktionen aus.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)


</dt> <dd>

Beschreibt ein Element, das zwischen Zuständen besteht, d. h., es ist nicht vollständig im vorherigen Zustand oder im nächsten Zustand verfügbar. Dieser Wert sollte verwendet werden, wenn andere Werte, die auf einen Übergang zu einem bestimmten Zustand hindeuten, nicht anwendbar sind.

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)


</dt> <dd>

Beschreibt ein Element, das sich im Dienst und betriebsbereit befindet.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (0X8000..)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**".**Status Beschreibungen**")
</dt> </dl>

Enthält Indikatoren zum aktuellen Status des Elements. Der erste Wert der **OperationalStatus** -Eigenschaft sollte den primären Status für das Element enthalten.

> [!Note]  
> Die **OperationalStatus** -Eigenschaft ersetzt die veraltete **Status** -Eigenschaft. Aufgrund der weit verbreiteten Verwendung der Eigenschaft " **Status** " in Verwaltungs Anwendungen wird dringend empfohlen, dass Anbieter oder Instrumentation die Eigenschaften " **Status** " und " **OperationalStatus** " bereitstellen. Bei instrumentiertem **Status** sollte auch der primäre Status des Elements bereitgestellt werden, da es sich um eine einwertige Eigenschaft handelt.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**OK** (2)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (3** )


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (4)


</dt> <dd>

Das Element funktioniert, erfordert jedoch Aufmerksamkeit. Beispiele für "betonte" Zustände sind Überlastung, überlastet usw.

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (5)


</dt> <dd>

Ein Element funktioniert nominisch, Vorhersage eines Fehlers in naher Zukunft.

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (6)


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (7)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (8)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (9** )


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (10)


</dt> <dd>

Ein ordnungsgemäßes Beenden ist aufgetreten.

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (11)


</dt> <dd>

Ein Element, das konfiguriert, gewartet, bereinigt oder anderweitig verwaltet wird.

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (12)


</dt> <dd>

Das Überwachungssystem kennt dieses Element, aber es war noch nie in der Lage, Kommunikation mit ihm herzustellen.

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (13)


</dt> <dd>

Das managedsystem-Element ist bekanntermaßen vorhanden und wurde in der Vergangenheit erfolgreich kontaktiert, ist aber zurzeit nicht erreichbar.

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (14)


</dt> <dd>

Eine abrupte Beendigung, bei der der Zustand und die Konfiguration des Elements möglicherweise aktualisiert werden müssen, ist aufgetreten.

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (15)


</dt> <dd>

Das Element ist inaktiv oder inaktiv.

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (16)


</dt> <dd>

Dieses Element ist möglicherweise "OK", aber dass ein anderes Element, von dem es abhängt, fehlerhaft ist. Ein Beispiel hierfür ist ein Netzwerkdienst oder ein Endpunkt, der aufgrund von Netzwerkproblemen auf niedrigerer Ebene nicht funktionsfähig ist.

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (17)


</dt> <dd>

Das Element hat seinen Vorgang abgeschlossen.

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Energie Modus** (18)


</dt> <dd>

Das-Element verfügt über zusätzliche Energiemodell Informationen, die in der zugeordneten powermanagementservice-Zuordnung enthalten sind.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (0X8000..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**".**Detailedstatus**","**CIM \_ ManagedSystemElement**.**Healthstate**")
</dt> </dl>

Gibt einen Statuswert auf hoher Ebene an.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft (2** )


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (0X8000..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ ManagedSystemElement**".**OperationalStatus**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Gibt den primären Status des Objekts an.

> [!Note]  
> Diese Eigenschaft ist veraltet. Sie wird durch die Eigenschaft **OperationalStatus** ersetzt. Wenn Sie sich für die Verwendung der **Status** -Eigenschaft für die Abwärtskompatibilität entscheiden, sollte Sie für die **OperationalStatus** -Eigenschaft sekundär sein.

 

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Fehler")


</dt> <dd></dd> <dt>



 ("Heruntergestuft")


</dt> <dd></dd> <dt>



 ("Unbekannt")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Wird gestartet")


</dt> <dd></dd> <dt>



 ("Wird beendet")


</dt> <dd></dd> <dt>



 ("Dienst")


</dt> <dd></dd> <dt>



 ("Gestresst")


</dt> <dd></dd> <dt>



 ("Nicht wiederherstellen")


</dt> <dd></dd> <dt>



 ("Kein Kontakt")


</dt> <dd></dd> <dt>



 ("Verlorene comm")


</dt> <dd></dd> <dt>



 ("Beendet")


</dt> <dd></dd> </dl>

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**".**OperationalStatus**")
</dt> </dl>

Gibt Beschreibungen der entsprechenden Werte im **OperationalStatus** -Array an. Wenn z. b. ein Element in der **OperationalStatus** -Eigenschaft den Wert **stoppt**, enthält das-Element am gleichen Array Index in dieser Eigenschaft möglicherweise eine Erläuterung, warum ein Objekt beendet wird.

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

[**CIM- \_ managedelta**](cim-managedelement.md)
</dt> </dl>

 

