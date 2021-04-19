---
description: Beschreibt die virtuellen Aspekte eines virtuellen Systems durch eine Reihe von virtualisierungsspezifischen Eigenschaften. CIM \_ virtualsystemsettingdata wird auch als Klasse der obersten Ebene der virtuellen Systemkonfigurationen verwendet.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368921"
---
# <a name="cim_virtualsystemsettingdata-class"></a>CIM \_ virtualsystemsettingdata-Klasse

Beschreibt die virtuellen Aspekte eines virtuellen Systems durch eine Reihe von virtualisierungsspezifischen Eigenschaften. **CIM \_ Virtualsystemsettingdata** wird auch als Klasse der obersten Ebene der virtuellen Systemkonfigurationen verwendet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Member

Die **CIM- \_ virtualsystemsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ virtualsystemsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Automatikrecoveryaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die für das virtuelle System auszuführende Aktion, wenn die vom virtuellen System ausgeführte Software ausfällt. Zu den von dieser Eigenschaft behandelten Fehlern zählen nur solche, die von der Host Plattform erkannt werden, z. b. eine nicht unter brechbare Bedingung für den Wartezustand.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Neu starten** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Momentaufnahme** wiederherstellen (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Automaticshutdownaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Aktion, die beim Herunterfahren des Hosts für das virtuelle System ausgeführt werden soll.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Ausschalten** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Zustand speichern** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Herunter** fahren (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Automaticstartupaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Aktion, die beim Starten des Hosts auf dem virtuellen System ausgeführt werden soll.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Neu starten, wenn zuvor aktiv** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Immer starten** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Automaticstartupactiondelay**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerung für die Start Aktion. Dieser Wert ist eine Intervall Variante des **DateTime** -Datentyps.

</dd> <dt>

**Automaticstartupactionsequencenumschlag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Sequenznummer für die Aktivierung des virtuellen Systems, wenn das Host System gestartet wird. Eine niedrigere Zahl deutet auf eine frühere Aktivierung hin. Wenn eine oder mehrere Konfigurationen denselben Wert aufweisen, ist die Sequenz implementierungsabhängig. Der Wert "0" gibt an, dass die Sequenz implementierungsabhängig ist.

</dd> <dt>

**Configurationdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Dateipfad des Verzeichnisses, in dem Informationen zur Konfiguration des virtuellen Systems gespeichert werden. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad der Datei, in der Informationen über die Konfiguration des virtuellen Systems gespeichert werden. Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die eindeutige ID der virtuellen Systemkonfiguration.

> [!Note]  
> **Configurationid** unterscheidet sich von der **InstanceId** und wird von der Implementierung einem virtuellen System oder einer virtuellen Systemkonfiguration zugewiesen. **Configurationid** ist kein Schlüssel, und der gleiche Wert kann für mehr als eine Instanz auftreten.

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der virtuellen Systemkonfiguration.

</dd> <dt>

**Logdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Dateipfad des Verzeichnisses, in dem die Protokollinformationen für das virtuelle System gespeichert werden. Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**Hinweise**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das vom Benutzer bereitgestellte Notizen enthält, die mit dem virtuellen System verknüpft sind.

</dd> <dt>

**Wiederherstellbare Datei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der Datei, in der Wiederherstellungs bezogene Informationen des virtuellen Systems gespeichert werden. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**Snapshotdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad des Verzeichnisses, in dem Informationen zu virtuellen System Momentaufnahmen gespeichert werden. Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**Suspenddataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad des Verzeichnisses, in dem die zusammenhängenden Informationen zum virtuellen System gespeichert werden. Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**Austauschen von Daten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Dateipfad des Verzeichnisses, in dem die Auslagerungs Dateien des virtuellen Systems gespeichert werden. Der relative Pfad wird an den Wert der **configurationdataroot** -Eigenschaft angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**Virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name für das System innerhalb der Virtualisierungsplattform. **Virtualsystemtifier** ist nicht der Hostname, der der im virtuellen System laufenden Betriebssystem Instanz zugewiesen ist, oder es handelt sich um eine IP-Adresse oder Mac-Adresse, die einem der zugehörigen Netzwerkports zugewiesen ist.

Der **virtualsystemtifier** kann Implementierungs spezifische Regeln enthalten, z. b. einfache Muster oder einen regulären Ausdruck, der von der Implementierung beim Festlegen von **virtualsystemdentifier** interpretiert werden kann.

</dd> <dt>

**Virtualsystemtype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des virtuellen Systems.

> [!Note]  
> Wenn der Typ des virtuellen Systems unbekannt ist, muss dieser Wert auf "DMTF: Unknown" festgelegt werden.

 

Diese Eigenschaft wird mit dem folgenden Format der erweiterten Backus-Naur Form (ABNF) formatiert:

vs-Type = DMTF-Value/other-org-Value/Legacy-Value; DMTF-Value = "DMTF:" definierende-org ":" org-vs-Type; Other-org-value = Definition-org ":" org-vs-Type;

Der Wert des obigen ABNF-Formats lautet:

-   *DMTF: Wert*   ein durch DMTF definierter Eigenschafts Wert, der in der Beschreibung dieser Eigenschaft definiert ist.
-   *other-org-Value*   ist ein Eigenschafts Wert, der von einer anderen Geschäfts Entität als DMTF definiert wird und nicht in der Beschreibung dieser Eigenschaft definiert ist.
-   *Legacy-Wert*   ein Eigenschafts Wert, der von einer anderen Geschäfts Entität als DMTF definiert wird und nicht in der Beschreibung dieser Eigenschaft definiert ist. Diese Werte sind zulässig, werden jedoch im Laufe der Zeit als veraltet eingestuft.
-   *Definieren von-org ein Bezeichner*   für die Geschäfts Entität, die den virtuellen Systemtyp definiert. Er sollte ein urheberrechtlich geschütztes, mit einem oder einen mit einem Wert bezeichnetes oder einen eindeutigen Namen enthalten, der im Besitz der Geschäfts Entität Er darf nicht "DMTF" lauten und darf keinen Doppelpunkt enthalten.
-   *org-vs-geben Sie einen Bezeichner*   für den virtuellen Systemtyp innerhalb der definierenden Geschäfts Entität ein. Er sollte innerhalb von Definition-org eindeutig sein. "org-vs-Type" kann beliebige Zeichen verwenden, die für CIM-Zeichen folgen zulässig sind, mit Ausnahme der folgenden: U0000-U001F (Unicode-Steuerelemente), U0020 (Leerzeichen), U007F (Unicode-Steuerelemente) oder U0080-U009F (Unicode C1-Steuerelemente).
-   Wenn der Wert in Segmente strukturiert werden muss, sollten die Segmente durch einen einzelnen Doppelpunkt getrennt werden.
-   Die Werte dieser Eigenschaft sollten in der Groß-/Kleinschreibung verarbeitet werden. Sie sollen nicht als Anzeige Name, sondern Programm gesteuert verarbeitet werden, und es sollte kurz sein.

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

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




