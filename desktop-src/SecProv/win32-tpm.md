---
description: Stellt den Trusted Platform Module (TPM) dar, einen Hardwaresicherheitschip, der einen Vertrauensstamm für ein Computersystem bereitstellt.
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
ms.openlocfilehash: 53fbe055e469dc4327ae747ab3e20873724923980f1e765d266a5f8143b545c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004018"
---
# <a name="win32_tpm-class"></a>Win32 \_ Tpm-Klasse

Die **Win32 \_ Tpm-Klasse** stellt den Trusted Platform Module (TPM) dar, einen Hardwaresicherheitschip, der einen Vertrauensstamm für ein Computersystem bereitstellt.

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

Die **Win32 \_ Tpm-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ Tpm-Klasse** verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBlockedCommand**](addblockedcommand-win32-tpm.md)                                 | Fügt der lokalen Liste der auf Windows blockierten Befehle einen TPM-Befehl hinzu.<br/>                                                                                                             |
| [**ChangeOwnerAuth**](changeownerauth-win32-tpm.md)                                     | Ändert den Wert der TPM-Besitzerautorisierung.<br/>                                                                                                                                       |
| [**Klar**](clear-win32-tpm.md)                                                         | Setzt das TPM auf den standardseitigen Zustand zurück.<br/>                                                                                                                                     |
| [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md)                               | Konvertiert eine vom Benutzer bereitgestellte Passphrase in einen 20-Byte-Besitzerautorisierungswert, der für die Interaktion mit dem TPM verwendet werden kann.<br/>                                                            |
| [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)                   | Erstellt ein 2048-Bit-Endorsement Key-Paar auf dem TPM.<br/>                                                                                                                              |
| [**Deaktivieren**](disable-win32-tpm.md)                                                     | Ermöglicht dem TPM-Besitzer, das TPM zu deaktivieren.<br/>                                                                                                                                         |
| [**Aktivieren**](enable-win32-tpm.md)                                                       | Ermöglicht dem TPM-Besitzer, das TPM zu aktivieren.<br/>                                                                                                                                          |
| [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)               | Ruft den ausstehenden physischen TPM-Anwesenheitsvorgang ab und gibt den Vorgang zurück. Verwenden Sie die [**SetPhysicalPresenceRequest-Methode,**](setphysicalpresencerequest-win32-tpm.md) um einen Vorgang anzufordern.<br/> |
| [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)             | Ruft die Ergebnisse eines physischen TPM-Anwesenheitsvorgangs ab, der ausgeführt wurde, und gibt sie zurück.<br/>                                                                                          |
| [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)         | Gibt die Benutzeraktion an, die zum Ausführen eines physischen TPM-Anwesenheitsvorgangs erforderlich ist.<br/>                                                                                           |
| [**IsActivated**](isactivated-win32-tpm.md)                                             | Gibt an, ob das TPM aktiviert ist.<br/>                                                                                                                                          |
| [**IsCommandBlocked**](iscommandblocked-win32-tpm.md)                                   | Gibt an, ob der TPM-Befehl unter diesem Betriebssystem ausgeführt werden kann.<br/>                                                                                                              |
| [**IsCommandPresent**](iscommandpresent-win32-tpm.md)                                   | Gibt an, ob ein TPM-Befehl von diesem Computer unterstützt wird.<br/>                                                                                                                   |
| [**isEnabled**](isenabled-win32-tpm.md)                                                 | Gibt an, ob das TPM aktiviert ist.<br/>                                                                                                                                            |
| [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md)             | Gibt an, ob das TPM über ein Endorsement Key-Paar verfügt.<br/>                                                                                                                           |
| [**IsOwned**](isowned-win32-tpm.md)                                                     | Gibt an, ob das TPM über einen Besitzer verfügt.<br/>                                                                                                                                          |
| [**IsOwnerClearDisabled**](isownercleardisabled-win32-tpm.md)                           | Gibt an, ob der TPM-Besitzer das TPM löschen kann.<br/>                                                                                                                               |
| [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)                               | Gibt an, ob ein TPM-Besitzer installiert werden kann.<br/>                                                                                                                                  |
| [**IsPhysicalClearDisabled**](isphysicalcleardisabled-win32-tpm.md)                     | Gibt an, ob ein physischer TPM-Anwesenheitsvorgang das TPM löschen kann.<br/>                                                                                                           |
| [**IsPhysicalPresenceHardwareEnabled**](isphysicalpresencehardwareenabled-win32-tpm.md) | Gibt an, ob dieser Computer einen dedizierten Hardwarepfad unterstützt, um physische Präsenz zu signalisieren.<br/>                                                                                  |
| [**IsSrkAuthCompatible**](issrkauthcompatible-win32-tpm.md)                             | Gibt an, ob die SRK-Autorisierung (Storage Root Key) mit Windows kompatibel ist.<br/>                                                                                           |
| [**RemoveBlockedCommand**](removeblockedcommand-win32-tpm.md)                           | Entfernt einen TPM-Befehl aus der lokalen Liste der Befehle, die durch Windows blockiert werden.<br/>                                                                                                        |
| [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)                                   | Setzt den Time out-Zeitraum oder einen anderen Mechanismus zurück, den TPM-Hersteller implementieren, um sich vor Wörterbuchangriffen auf das TPM zu schützen.<br/>                                                 |
| [**ResetSrkAuth**](resetsrkauth-win32-tpm.md)                                           | Setzt den SRK-Autorisierungswert (Storage Root Key) zurück, um mit Windows kompatibel zu sein.<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | Führt einen Selbsttest des TPM aus und gibt das Ergebnis zurück.<br/>                                                                                                                          |
| [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)               | Fordert die Ausführung eines physischen TPM-Anwesenheitsvorgangs an.<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | Installiert einen Besitzer für das TPM.<br/>                                                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Tpm-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**IsActivated \_ InitialValue**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das TPM aktiviert ist.

**TRUE,** wenn das Gerät aktiviert ist (d. h. wenn **IsActivated \_ InitialValue** true ist), andernfalls **FALSE.**

Dieser Wert wird gespeichert, wenn die Klasse instanziiert wird. Es ist möglich, dass das TPM den Zustand zwischen der Instanziierung und beim Überprüfen dieses Werts ändert. Verwenden Sie die [**IsActivated-Methode,**](isactivated-win32-tpm.md) um zu überprüfen, ob das TPM in Echtzeit aktiviert ist.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**IsEnabled \_ InitialValue**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das TPM aktiviert ist.

**TRUE,** wenn das Gerät aktiviert ist (d. h. **wenn IsEnabled \_ InitialValue** true ist), andernfalls **FALSE.**

Dieser Wert wird gespeichert, wenn die Klasse instanziiert wird. Es ist möglich, dass das TPM den Zustand zwischen der Instanziierung und beim Überprüfen dieses Werts ändert. Verwenden Sie die [**IsEnabled-Methode,**](isenabled-win32-tpm.md) um zu überprüfen, ob das TPM in Echtzeit aktiviert ist.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**IsOwned \_ InitialValue**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das TPM über einen Besitzer verfügt.

**TRUE,** wenn das Gerät über einen Besitzer verfügt (d. h. **wenn IsOwned \_ InitialValue** true ist), andernfalls **FALSE.**

Dieser Wert wird gespeichert, wenn die Klasse instanziiert wird. Es ist möglich, dass das TPM den Zustand zwischen der Instanziierung und beim Überprüfen dieses Werts ändert. Verwenden Sie die [**IsOwned-Methode,**](isowned-win32-tpm.md) um zu überprüfen, ob sich das TPM in Echtzeit im Besitz des TPM befindet.

**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**ManufacturerId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die identifizierenden Informationen, die den TPM-Hersteller eindeutig benennen.

Wenn die Daten nicht verfügbar sind, wird 0 zurückgegeben.

Dieser ganzzahlige Wert kann in einen Zeichenfolgenwert übersetzt werden, indem jedes Byte als ASCII-Zeichen interpretiert wird. Beispielsweise kann ein ganzzahliger Wert von 1414548736 in die folgenden 4 Bytes unterteilt werden: 0x54, 0x50, 0x4D und 0x00. Wenn die Zeichenfolge von links nach rechts interpretiert wird, wird dieser ganzzahlige Wert in den Zeichenfolgenwert "TPM" übersetzt.

</dd> <dt>

**ManufacturerVersion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die vom Hersteller angegebene Version des TPM.

Wenn die Daten nicht verfügbar sind, wird "Nicht unterstützt" zurückgegeben.

</dd> <dt>

**ManufacturerVersionInfo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Weitere herstellerspezifische Versionsinformationen für das TPM.

Wenn die Daten nicht verfügbar sind, wird "Nicht unterstützt" zurückgegeben.

</dd> <dt>

**PhysicalPresenceVersionInfo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version der Schnittstelle für physische Präsenz, ein Kommunikationsmechanismus, der zum Ausführen von Gerätevorgängen verwendet wird, die physische Präsenz erfordern, die der Computer unterstützt.

Diese Schnittstelle muss verfügbar sein, um PHYSISCHE TPM-Anwesenheitsvorgänge auszuführen. Die **Win32 \_ Tpm-Methoden** [**SetPhysicalPresenceRequest,**](setphysicalpresencerequest-win32-tpm.md) [**GetPhysicalPresenceRequest,**](getphysicalpresencerequest-win32-tpm.md) [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)und [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) machen die Funktionen der Physical Presence Interface verfügbar.

Wenn die Daten nicht verfügbar sind, wird "Nicht unterstützt" zurückgegeben.

</dd> <dt>

**SpecVersion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version der TCG-Spezifikation (Trusted Computing Group), die das TPM unterstützt. Dieser Wert umfasst die Haupt- und Nebenversion der TCG-Spezifikation, die Spezifikationsrevisionsebene und die Errata-Revisionsebene. Alle Werte sind hexadezimal. Eine Versionsinformation von "1.2, 2, 0" gibt beispielsweise an, dass das Gerät in die TCG-Spezifikation Version 1.2, Revisionsebene 2 und ohne Errata implementiert wurde.

Wenn die Daten nicht verfügbar sind, wird "Nicht unterstützt" zurückgegeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



 

 
