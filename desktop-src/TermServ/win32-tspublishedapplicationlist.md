---
title: Win32_TSPublishedApplicationList-Klasse
description: Stellt die Liste der Programme dar, die in der Liste der RemoteApp-Programme auf einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) enthalten sind.
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplicationList-Klasse Remotedesktopdienste
- Win32_TSPublishedApplicationList Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040475"
---
# <a name="win32_tspublishedapplicationlist-class"></a>Win32 \_ tspublishedapplicationlist-Klasse

Stellt die Liste der Programme dar, die in der Liste der RemoteApp-Programme auf einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) enthalten sind.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a>Member

Die **Win32 \_ tspublishedapplicationlist** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ tspublishedapplicationlist** -Klasse verfügt über diese Eigenschaften.

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

**Deaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der RD-Sitzungshost Server die Programme einschränkt, die ein Benutzer bei der anfänglichen Verbindung mit den Programmen in der RemoteApp-Programmliste starten darf.

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

**Policysourcedeaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wo die **Deaktivierte** Eigenschaft konfiguriert ist. Mögliche Werte:

<dt>

0
</dt> <dd>

Die Einstellung wird auf dem Server über RemoteApp-Manager oder den RemoteApp-WMI-Anbieter konfiguriert.

</dd> <dt>

1
</dt> <dd>

Die Einstellung wird durch die Gruppenrichtlinie konfiguriert.

</dd> <dt>

2
</dt> <dd>

Die Einstellung ist nicht konfiguriert. Der Standardwert **false** wird für die **Deaktivierte** Eigenschaft verwendet.

</dd> </dl>

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um Eigenschaften mithilfe dieser Klasse festzulegen.

Durch die **Deaktivierte** Eigenschaft wird nicht verhindert, dass Benutzer nicht aufgelistete Programme remote starten, nachdem Sie mithilfe eines RemoteApp-Programms eine Verbindung mit dem RD-Sitzungshost Server hergestellt haben.

Die **Deaktivierte** Eigenschaft wird nur dann auf den Wert 2 festgelegt, wenn der folgende Registrierungs Eintrag fehlt:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminalserver** \\ **\appallowlist** \\ **fdisabledallowlist**

Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6. Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

