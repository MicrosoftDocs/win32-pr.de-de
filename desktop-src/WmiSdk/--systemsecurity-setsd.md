---
description: Legt die Sicherheitsbeschreibung für den Namespace fest, mit dem ein Benutzer verbunden ist. Diese Methode erfordert einen Sicherheitsdeskriptor im binären Bytearrayformat. Wenn Sie ein Skript schreiben, verwenden Sie die SetSecurityDescriptor-Methode.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: SetSD-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 04da59b6370e2e9a381f2e3889b75ac37cb926e54c46cc0e616ec5353ed6f665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132033"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>SetSD-Methode der \_ \_ SystemSecurity-Klasse

Die **SetSD-Methode** legt den Sicherheitsdeskriptor für den Namespace fest, mit dem ein Benutzer verbunden ist. Diese Methode erfordert einen Sicherheitsdeskriptor im binären Bytearrayformat. Wenn Sie ein Skript schreiben, verwenden Sie die [**SetSecurityDescriptor-Methode.**](setsecuritydescriptor-method-in-class---systemsecurity.md) Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md) und [Ändern der Zugriffssicherheit für sicherungsfähige Objekte.](changing-access-security-on-securable-objects.md)

Wenn Sie in C++ programmieren, können Sie den binären Sicherheitsdeskriptor mit [sddl](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und den Konvertierungsmethoden [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.

Ein Benutzer muss über die **\_ WRITE-DAC-Berechtigung** verfügen, und standardmäßig verfügt ein Administrator über diese Berechtigung. Der einzige Teil der Sicherheitsbeschreibung, der verwendet wird, ist der nicht überwachte Zugriffssteuerungseintrag (ACE) in der DACL (Discretionary Access Control List). Durch Festlegen des **CONTAINER \_ INHERIT-Flags** in den ACEs wirkt sich der Sicherheitsdeskriptor auf untergeordnete Namespaces aus. AcEs zum Zulassen und Verweigern sind zulässig.

> [!Note]  
> Da Verweigerungs- und Zulassungs-ACEs in einer DACL zulässig sind, ist die Reihenfolge der ACEs wichtig. Weitere Informationen finden Sie unter [Sortieren von ACEs in einer DACL.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

 

## <a name="syntax"></a>Syntax


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SD* \[ In\]
</dt> <dd>

Bytearray, das den Sicherheitsdeskriptor bildet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **HRESULT** zurück, das den Status eines Methodenaufrufs angibt. Für Skripts und Visual Basic Anwendungen kann das Ergebnis aus [OutParameters.ReturnValue](parsing-outparameters-objects.md)abgerufen werden. Weitere Informationen finden Sie unter [Erstellen von InParameters-Objekten und Analysieren von OutParameters-Objekten.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

In der folgenden Liste sind die Rückgabewerte aufgeführt, die für **SetSD** von Bedeutung sind.

<dl> <dt>

**S \_ OK**
</dt> <dd>

Die Methode wurde erfolgreich ausgeführt.

</dd> <dt>

**WBEM \_ E \_ ACCESS \_ DENIED**
</dt> <dd>

Der Aufrufer verfügt nicht über ausreichende Rechte zum Aufrufen dieser Methode.

</dd> <dt>

**WBEM \_ \_ E-METHODE \_ DEAKTIVIERT**
</dt> <dd>

Es wurde versucht, diese Methode unter einem Betriebssystem auszuführen, das sie nicht unterstützt.

</dd> <dt>

**WBEM \_ E \_ UNGÜLTIGES \_ OBJEKT**
</dt> <dd>

SD bestanden keine grundlegenden Gültigkeitstests.

</dd> <dt>

**WBEM \_ E \_ INVALID \_ PARAMETER**
</dt> <dd>

SD ist aufgrund einer der folgenden Punkte ungültig:

-   DACL fehlt.
-   DACL ist ungültig.
-   Für ACE ist das **WBEM \_ FULL \_ WRITE \_ REP-Flag** festgelegt, und das **WBEM \_ PARTIAL WRITE \_ \_ REP-** oder **WBEM \_ WRITE \_ PROVIDER-Flag** ist nicht festgelegt.
-   Für ACE ist das INHERIT **\_ ONLY \_ ACE-Flag** ohne das **CONTAINER INHERIT \_ \_ ACE-Flag** festgelegt.
-   Ace hat ein unbekanntes Zugriffsbit festgelegt.
-   Ace hat ein Flag festgelegt, das nicht in der Tabelle enthalten ist.
-   ACE weist einen Typ auf, der nicht in der Tabelle enthalten ist.
-   Der Besitzer und die Gruppe fehlen in der SD.

Weitere Informationen zu den ACE-Flags (Access Control Entry, Zugriffssteuerungseintrag) finden Sie unter [WMI-Sicherheitskonstanten.](wmi-security-constants.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zum programmgesteuerten oder manuellen Ändern der Namespacesicherheit finden Sie unter [Schützen von WMI-Namespaces.](securing-wmi-namespaces.md)

## <a name="examples"></a>Beispiele

Das folgende Skript zeigt, wie **Sie setSD** verwenden, um den Namespacesicherheitsdeskriptor für den Stammnamespace festzulegen und in das bytearray zu ändern, das in *strSD* gezeigt wird.


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



Im folgenden C#-Codebeispiel wird System.Security.AccessControl.RawSecurityDescriptor verwendet, um neue CommonAce-Objekte in RawSecurityDescriptor.DiscretionaryAcl aufzuzählen, einzufügen und zu entfernen und sie dann wieder in ein Bytearray zu konvertieren, um es über SetSD zu speichern. Ein SecurityIdentifier kann mit NTAccount und Translate abgerufen werden.


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[WMI-Sicherheitskonstanten](wmi-security-constants.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> </dl>

 

