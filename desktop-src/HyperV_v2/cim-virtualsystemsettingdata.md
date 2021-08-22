---
description: Beschreibt die virtuellen Aspekte eines virtuellen Systems durch eine Reihe von virtualisierungsspezifischen Eigenschaften. CIM VirtualSystemSettingData wird auch als Klasse der obersten Ebene \_ von Konfigurationen des virtuellen Systems verwendet.
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
ms.openlocfilehash: 1caed7797343eac9babd320af42fd6c9aaaffeff054211cc55bda0d437582d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068490"
---
# <a name="cim_virtualsystemsettingdata-class"></a>CIM \_ VirtualSystemSettingData-Klasse

Beschreibt die virtuellen Aspekte eines virtuellen Systems durch eine Reihe von virtualisierungsspezifischen Eigenschaften. **CIM \_ VirtualSystemSettingData** wird auch als Klasse der obersten Ebene von Konfigurationen des virtuellen Systems verwendet.

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

Die **CIM \_ VirtualSystemSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ VirtualSystemSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Aktion, die für das virtuelle System ausgeführt werden soll, wenn die vom virtuellen System ausgeführte Software ausfällt. Die von dieser Eigenschaft behobenen Fehler umfassen nur diejenigen, die von der Hostplattform erkannt werden können, z. B. eine bedingung für einen nicht unterbrechbaren Wartezustand.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Neustart** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Wiederherstellen der Momentaufnahme** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Aktion, die für das virtuelle System ausgeführt werden soll, wenn der Host heruntergefahren wird.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Deaktivieren** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Speichern des Zustands** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Herunterfahren** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Aktion, die auf dem virtuellen System ausgeführt werden soll, wenn der Host gestartet wird.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Neustart, wenn er zuvor aktiv war** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Immer starten** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerung für die Startaktion. Dieser Wert ist eine Intervallvariante des **datetime-Datentyps.**

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Sequenznummer für die Aktivierung des virtuellen Systems, wenn das Hostsystem gestartet wird. Eine niedrigere Zahl gibt eine frühere Aktivierung an. Wenn eine oder mehrere Konfigurationen den gleichen Wert anzeigen, ist die Sequenz von der Implementierung abhängig. Der Wert "0" gibt an, dass die Sequenz von der Implementierung abhängig ist.

</dd> <dt>

**ConfigurationDataRoot**
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

Der relative Pfad der Datei, in der Informationen zur Konfiguration des virtuellen Systems gespeichert werden. Der relative Pfad wird an den Wert der **ConfigurationDataRoot-Eigenschaft** angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die eindeutige ID der Konfiguration des virtuellen Systems.

> [!Note]  
> **ConfigurationID** ist anders als **InstanceID** und wird von der Implementierung einem virtuellen System oder einer Konfiguration des virtuellen Systems zugewiesen. **ConfigurationID** ist kein Schlüssel, und der gleiche Wert kann für mehrere Instanzen auftreten.

 

</dd> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration des virtuellen Systems.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Dateipfad des Verzeichnisses, in dem Protokollinformationen für das virtuelle System gespeichert werden. Der relative Pfad wird an den Wert der **ConfigurationDataRoot-Eigenschaft** angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**Notizen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das vom Benutzer bereitgestellte Notizen enthält, die mit dem virtuellen System verknüpft sind.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der Datei, in der wiederherstellungsbezogene Informationen des virtuellen Systems gespeichert werden. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad des Verzeichnisses, in dem Informationen zu Momentaufnahmen virtueller Systeme gespeichert werden. Der relative Pfad wird an den Wert der **ConfigurationDataRoot-Eigenschaft** angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad des Verzeichnisses, in dem angehaltene Informationen zum virtuellen System gespeichert werden. Der relative Pfad wird an den Wert der **ConfigurationDataRoot-Eigenschaft** angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Dateipfad des Verzeichnisses, in dem Auslagerungsdateien des virtuellen Systems gespeichert werden. Der relative Pfad wird an den Wert der **ConfigurationDataRoot-Eigenschaft** angefügt. Das Format dieser Eigenschaft ist ein URI, der auf RFC 2079 basiert.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name für das System innerhalb der Virtualisierungsplattform. **VirtualSystemIdentifier** ist weder der Hostname, der der betriebssysteminstanz zugewiesen ist, die im virtuellen System ausgeführt wird, noch ist er eine IP-Adresse oder MAC-Adresse, die einem seiner Netzwerkports zugewiesen ist.

**VirtualSystemIdentifier kann** implementierungsspezifische Regeln enthalten, z. B. einfache Muster oder einen regulären Ausdruck, der von der Implementierung interpretiert werden kann, wenn **VirtualSystemIdentifier festgelegt wird.**

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des virtuellen Systems.

> [!Note]  
> Wenn der virtuelle Systemtyp unbekannt ist, muss dieser Wert auf "DMTF:unknown" festgelegt werden.

 

Diese Eigenschaft wird im folgenden ABNF-Format (Augmented BackusFs) formatiert:

vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;

Der Wert des oben genannten ABNF-Formats ist:

-   *dmtf-value*   ein von DMTF definierter Eigenschaftswert, der in der Beschreibung dieser Eigenschaft definiert ist.
-   *other-org-value*   ist ein Eigenschaftswert, der von einer anderen Geschäftsentität als DMTF definiert wird und nicht in der Beschreibung dieser Eigenschaft definiert ist.
-   *legacy-value*   ein Eigenschaftswert, der von einer anderen Geschäftsentität als DMTF definiert wird und nicht in der Beschreibung dieser Eigenschaft definiert ist. Diese Werte sind zulässig, sollten aber im Laufe der Zeit als veraltet gelten.
-   *definitioning-org ein*   Bezeichner für die Geschäftsentität, die den typ des virtuellen Systems definiert. Sie sollte einen urheberrechtlich geschützten, markenierten oder eindeutigen Namen enthalten, der im Besitz der Geschäftseinheit ist. Er sollte nicht "DMTF" sein und darf keinen Doppelpunkt enthalten.
-   *org-vs-type einen*   Bezeichner für den virtuellen Systemtyp innerhalb der definierenden Geschäftsentität ein. Sie sollte innerhalb von defining-org eindeutig sein. org-vs-type kann beliebige Zeichen verwenden, die für CIM-Zeichenfolgen zulässig sind, mit Ausnahme der folgenden Zeichen: U0000-U001F (Unicode C0-Steuerelemente), U0020 (Leerzeichen), U007F (Unicode C0-Steuerelemente) oder U0080-U009F (Unicode C1-Steuerelemente).
-   Wenn der Wert in Segmente strukturiert werden muss, sollten die Segmente durch einen einzelnen Doppelpunkt getrennt werden.
-   Bei den Werten dieser Eigenschaft muss die Schreibung beachtet werden. Sie sollen programmgesteuert verarbeitet werden, anstatt ein Anzeigename zu sein, und sollten kurz sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




