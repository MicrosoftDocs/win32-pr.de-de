---
title: Win32_TerminalSetting-Klasse
description: Stellt die Einstellungen dar, die auf ein Terminal angewendet werden können.
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Win32_TerminalSetting-Klasse Remotedesktopdienste
- Win32_TerminalSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341026"
---
# <a name="win32_terminalsetting-class"></a>Win32 \_ TerminalSetting-Klasse

Die **Win32 \_ TerminalSetting** -WMI-Klasse stellt die Einstellungen dar, die auf ein Terminal angewendet werden können.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TerminalSetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TerminalSetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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


</dt> <dd></dd> </dl>

</dd> <dt>

**Terminal Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Terminals.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[**Win32 \_ Terminalservice**](win32-terminalservice.md)
</dt> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

