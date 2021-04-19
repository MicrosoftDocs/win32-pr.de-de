---
description: Stellt den Trusted Platform Module (TPM) dar, einen Hardware Sicherheits Chip, der eine Vertrauensstellung für ein Computersystem bereitstellt.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356972"
---
# <a name="win32_tpm-class"></a>Win32- \_ TPM-Klasse

Die **Win32- \_ TPM** -Klasse stellt die Trusted Platform Module (TPM) dar, einen Hardware Sicherheits Chip, der eine Vertrauensstellung für ein Computersystem bereitstellt.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a>Member

Die **Win32- \_ TPM** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ TPM** -Klasse verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addblockedcommand**](addblockedcommand-win32-tpm.md)                                 | Fügt der lokalen Liste von Befehlen, die unter Windows blockiert sind, einen TPM-Befehl hinzu.<br/>                                                                                                             |
| [**Changebesitzauth**](changeownerauth-win32-tpm.md)                                     | Ändert den TPM-Besitzer Autorisierungs Wert.<br/>                                                                                                                                       |
| [**Klartext**](clear-win32-tpm.md)                                                         | Setzt das TPM auf seine Werkseinstellungen zurück.<br/>                                                                                                                                     |
| [**Converttbesitzauth**](converttoownerauth-win32-tpm.md)                               | Konvertiert eine vom Benutzer bereitgestellte Passphrase in einen 20-Byte-Besitzer Autorisierungs Wert, der für die Interaktion mit dem TPM verwendet werden kann.<br/>                                                            |
| [**"Kreateendorsegmentkeypair"**](createendorsementkeypair-win32-tpm.md)                   | Erstellt ein 2048-Bit-Endorsement Key-paar auf dem TPM.<br/>                                                                                                                              |
| [**Deaktivieren**](disable-win32-tpm.md)                                                     | Ermöglicht dem TPM-Besitzer, das TPM zu deaktivieren.<br/>                                                                                                                                         |
| [**Aktivieren**](enable-win32-tpm.md)                                                       | Ermöglicht dem TPM-Besitzer, das TPM zu aktivieren.<br/>                                                                                                                                          |
| [**Getphysicalpresencerequest**](getphysicalpresencerequest-win32-tpm.md)               | Ruft den ausstehenden TPM-Anwesenheits Vorgang ab und gibt ihn zurück. Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um einen Vorgang anzufordern.<br/> |
| [**Getphysicalpresenceresponse**](getphysicalpresenceresponse-win32-tpm.md)             | Ruft die Ergebnisse eines ausgeführten TPM-Vorgangs für physische Anwesenheit ab und gibt Sie zurück.<br/>                                                                                          |
| [**Getphysicalpresencetransition**](getphysicalpresencetransition-win32-tpm.md)         | Gibt die Benutzeraktion an, die erforderlich ist, um einen physischen TPM-Anwesenheits Vorgang auszuführen.<br/>                                                                                           |
| [**Isaktiviert**](isactivated-win32-tpm.md)                                             | Gibt an, ob das TPM aktiviert ist.<br/>                                                                                                                                          |
| [**Iscommandblockierte**](iscommandblocked-win32-tpm.md)                                   | Gibt an, ob der TPM-Befehl unter diesem Betriebssystem ausgeführt werden kann.<br/>                                                                                                              |
| [**Iscommandpresent**](iscommandpresent-win32-tpm.md)                                   | Gibt an, ob ein TPM-Befehl von diesem Computer unterstützt wird.<br/>                                                                                                                   |
| [**isEnabled**](isenabled-win32-tpm.md)                                                 | Gibt an, ob das TPM aktiviert ist.<br/>                                                                                                                                            |
| [**Isendorsementkeypaarpresent**](isendorsementkeypairpresent-win32-tpm.md)             | Gibt an, ob das TPM ein Endorsement Key-Paar hat.<br/>                                                                                                                           |
| [**Isowned**](isowned-win32-tpm.md)                                                     | Gibt an, ob das TPM über einen Besitzer verfügt.<br/>                                                                                                                                          |
| [**Isownercleardeaktiviert**](isownercleardisabled-win32-tpm.md)                           | Gibt an, ob der TPM-Besitzer das TPM löschen kann.<br/>                                                                                                                               |
| [**Isownershipallowed**](isownershipallowed-win32-tpm.md)                               | Gibt an, ob ein TPM-Besitzer installiert werden kann.<br/>                                                                                                                                  |
| [**Isphysicalcleardeaktiviert**](isphysicalcleardisabled-win32-tpm.md)                     | Gibt an, ob das TPM durch einen physischen TPM-Anwesenheits Vorgang gelöscht werden kann.<br/>                                                                                                           |
| [**Isphysicalpresencehardwareaktivierte**](isphysicalpresencehardwareenabled-win32-tpm.md) | Gibt an, ob dieser Computer einen dedizierten Hardware Pfad zum signalisieren physischer Präsenz unterstützt.<br/>                                                                                  |
| [**Issrkauthcompatible**](issrkauthcompatible-win32-tpm.md)                             | Gibt an, ob die SRK-Autorisierung (Storage Root Key) mit Windows kompatibel ist.<br/>                                                                                           |
| [**Removeblockedcommand**](removeblockedcommand-win32-tpm.md)                           | Entfernt einen TPM-Befehl aus der lokalen Liste der Befehle, die von Windows blockiert werden.<br/>                                                                                                        |
| [**Resetauthlockout**](resetauthlockout-win32-tpm.md)                                   | Setzt den Timeout Zeitraum oder einen anderen Mechanismus zurück, den TPM-Hersteller implementiert, um Wörterbuchangriffe auf dem TPM zu schützen.<br/>                                                 |
| [**Resegzrkauth**](resetsrkauth-win32-tpm.md)                                           | Setzt den SRK-Autorisierungs Wert (Storage Root Key) so zurück, dass er mit Windows kompatibel ist.<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | Führt einen Selbsttest des TPM aus und gibt das Ergebnis zurück.<br/>                                                                                                                          |
| [**Setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md)               | Fordert die Ausführung eines physischen TPM-Anwesenheits Vorgangs an.<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | Installiert einen Besitzer für das TPM.<br/>                                                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ TPM** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Isaktivierter \_ InitialValue**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das TPM aktiviert ist.

**true** , wenn das Gerät aktiviert ist (d. h., wenn **isaktivierter \_ InitialValue** true ist), andernfalls **false**.

Dieser Wert wird gespeichert, wenn die-Klasse instanziiert wird. Das TPM kann den Status zwischen der Instanziierung und dem Zeitpunkt, zu dem Sie diesen Wert überprüfen, ändern. Verwenden Sie die [**isaktivierte**](isactivated-win32-tpm.md) Methode, um zu überprüfen, ob das TPM in Echtzeit aktiviert ist.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Isaktivierter \_ InitialValue**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das TPM aktiviert ist.

**true** , wenn das Gerät aktiviert ist (d. h., wenn **isaktivierter \_ InitialValue** true ist), andernfalls **false**.

Dieser Wert wird gespeichert, wenn die-Klasse instanziiert wird. Das TPM kann den Status zwischen der Instanziierung und dem Zeitpunkt, zu dem Sie diesen Wert überprüfen, ändern. Verwenden Sie die [**isaktivierte**](isenabled-win32-tpm.md) Methode, um zu überprüfen, ob das TPM in Echtzeit aktiviert ist.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Isowned \_ InitialValue**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das TPM über einen Besitzer verfügt.

**true** , wenn das Gerät über einen Besitzer verfügt (d. h., wenn der **isowned \_ InitialValue** true ist), andernfalls **false**.

Dieser Wert wird gespeichert, wenn die-Klasse instanziiert wird. Das TPM kann den Status zwischen der Instanziierung und dem Zeitpunkt, zu dem Sie diesen Wert überprüfen, ändern. Verwenden Sie die [**isowned**](isowned-win32-tpm.md) -Methode, um zu überprüfen, ob das TPM in Echtzeit gehört.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Manufacturerid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die identifizierenden Informationen, die den TPM-Hersteller eindeutig benennen.

Wenn die Daten nicht verfügbar sind, wird NULL zurückgegeben.

Dieser ganzzahlige Wert kann in einen Zeichen folgen Wert übersetzt werden, indem die einzelnen Bytes als ASCII-Zeichen interpretiert werden. Beispielsweise kann ein ganzzahliger Wert von 1414548736 in diese 4 Bytes unterteilt werden: 0x54, 0x50, 0x4D und 0x00. Wenn die Zeichenfolge von links nach rechts interpretiert wird, wird dieser ganzzahlige Wert in den Zeichen folgen Wert "TPM" übersetzt.

</dd> <dt>

**Manufacturerversion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die vom Hersteller angegebene TPM-Version.

Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.

</dd> <dt>

**Manufacturerversioninfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Weitere herstellerspezifische Versionsinformationen für das TPM.

Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.

</dd> <dt>

**Physicalpresenceversioninfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version der physischen Anwesenheits Schnittstelle, ein Kommunikationsmechanismus, der zum Ausführen von Geräte Vorgängen verwendet wird, die vom Computer unterstützt werden.

Diese Schnittstelle muss verfügbar sein, um TPM-Vorgänge zur physischen Anwesenheit auszuführen. Die **Win32 \_ TPM** -Methoden [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md), [**getphysicalpresencerequest**](getphysicalpresencerequest-win32-tpm.md), [**getphysicalpresencetransition**](getphysicalpresencetransition-win32-tpm.md)und [**getphysicalpresenceresponse**](getphysicalpresenceresponse-win32-tpm.md) machen die Funktionen der physischen Anwesenheits Schnittstelle verfügbar.

Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.

</dd> <dt>

**SpecVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version der Trusted Computing Group (TCG)-Spezifikation, die das TPM unterstützt. Dieser Wert umfasst die Spezifikation für die Haupt-und neben Version der TCG-Spezifikation, die Spezifikations Revisions Ebene und die Errata-Revisions Ebene. Alle Werte sind hexadezimal. Beispielsweise geben die Versionsinformationen "1,2, 2, 0" an, dass das Gerät in die TCG-Spezifikation Version 1,2, Revision Level 2 und ohne Errata implementiert wurde.

Wenn die Daten nicht verfügbar sind, wird "nicht unterstützt" zurückgegeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



 

 
