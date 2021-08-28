---
description: Schreibt eine aktualisierte Version der Sicherheitsbeschreibung, die den Zugriff auf den Drucker steuert.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: SetSecurityDescriptor-Methode der Win32_Printer Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8621c1977c4553f610299695c2c68a72f5a9d6f2ecfcbe6df46b8646c379c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958958"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a>SetSecurityDescriptor-Methode der Win32 \_ Printer-Klasse

Die **SetSecurityDescriptor-Methode** schreibt eine aktualisierte Version des Sicherheitsdeskriptors, die den Zugriff auf den Drucker steuert. Der Sicherheitsdeskriptor ist eine Instanz der [**Win32 \_ SecurityDescriptor-Klasse.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Weitere Informationen finden Sie unter Changing Access Security on Securable Objects (Ändern [der Zugriffssicherheit für sicherungsfähige Objekte).](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ In\]
</dt> <dd>

Der Sicherheitsdeskriptor, der dem Drucker zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Erfolgreicher Abschluss.

</dd> <dt>

**2**
</dt> <dd>

Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.

</dd> <dt>

**8**
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**9**
</dt> <dd>

Der Benutzer verfügt nicht über die erforderlichen Berechtigungen zum Ausführen der -Methode.

</dd> <dt>

**21**
</dt> <dd>

Ein im Methodenaufruf angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine DACL (Discretionary [*Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine Systemzugriffssteuerungsliste (SACL). [](/windows/desktop/SecGloss/s-gly) Weitere Informationen finden Sie unter [Access Control Listen.](/windows/desktop/SecAuthZ/access-control-lists)

Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) und [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).

Sie können sowohl die DACL als auch die SACL in der [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) aktualisieren, wenn Sie diese Methode aufrufen, aber Sie können auch nur die DACL oder nur die SACL aktualisieren.

Die folgenden Werte in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL, die SACL oder beide aktualisiert werden.

-   **\_SE DACL \_ PRESENT**

    Gibt an, dass die DACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.

-   **\_SE SACL \_ PRESENT**

    Gibt an, dass die SACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei. Zum Aktualisieren der SACL muss für das Konto die **Berechtigung SeSecurityPrivilege** aktiviert sein. Für die Skripterstellung ist der Berechtigungsname **SeSecurityPrivilege.** Weitere Informationen finden Sie unter [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).

Wenn der Gruppentreuhänder und die Eigenschaften des Besitzertreuhänders nicht **NULL sind,** werden sie aktualisiert. Andernfalls behält WMI die ursprünglichen Werte bei. Weitere Informationen finden Sie unter [WMI-Sicherheitsdeskriptorobjekte.](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)

Wenn eine neue SACL in einem Aufruf dieser Methode **NULL** ist, bleibt die Sicherheitsbeschreibung SACL für das sicherungsfähige Zielobjekt unverändert.

## <a name="examples"></a>Beispiele

Das [PowerShell-Beispiel Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) ersetzt die Berechtigungen (ACL) von einem Drucker zu einem anderen.

Im folgenden PowerShell-Codebeispiel wird beschrieben, wie der Sicherheitsdeskriptor für einen Drucker festgelegt wird.


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32-Drucker \_**](win32-printer.md)
</dt> <dt>

[**Berechtigungskonst constants**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-Sicherheitsdeskriptorobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

