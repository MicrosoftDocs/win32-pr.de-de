---
title: Win32_TSApplicationFileExtensions-Klasse
description: Die Dateinamen Erweiterungen, die von einer Anwendung auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server behandelt werden.
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Win32_TSApplicationFileExtensions-Klasse Remotedesktopdienste
- Win32_TSApplicationFileExtensions Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339589"
---
# <a name="win32_tsapplicationfileextensions-class"></a>Win32- \_ Klasse "tyapplicationfileextensions"

Beschreibt die Dateinamen Erweiterungen, die von einer Anwendung auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server behandelt werden.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ tyapplicationfileextensions** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zapplicationfileextensions** " verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Dateizuordnungen**](fileassociations-win32-tsapplicationfileextensions.md) | Scannt die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.<br/>     |
| [**Dateierweiterungen**](fileextensions-win32-tsapplicationfileextensions.md)     | Stellt eine Liste der Dateinamen Erweiterungen bereit, die von einer Anwendung behandelt werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ tyapplicationfileextensions** " verfügt über diese Eigenschaften.

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.

Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

