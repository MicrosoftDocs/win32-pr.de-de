---
description: Legt die Sicherheits Beschreibung für den Namespace fest, mit dem ein Benutzer verbunden ist. Diese Methode erfordert eine Sicherheits Beschreibung im Format des binären Byte Arrays. Wenn Sie ein Skript schreiben, verwenden Sie die SETSECURITYDESCRIPTOR-Methode.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Die Methode "SZD" der __SystemSecurity-Klasse
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
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347411"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Die Methode "-Methode" der \_ \_ Klasse "System Security"

Die **sezd-** Methode legt die Sicherheits Beschreibung für den Namespace fest, mit dem ein Benutzer verbunden ist. Diese Methode erfordert eine Sicherheits Beschreibung im Format des binären Byte Arrays. Wenn Sie ein Skript schreiben, verwenden Sie die [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md) -Methode. Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

Wenn Sie in C++ programmieren, können Sie den binären Sicherheits Deskriptor mithilfe von [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und die Konvertierungs Methoden [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.

Ein Benutzer muss über die Berechtigung zum **Schreiben von \_ DAC** verfügen, und ein Administrator verfügt standardmäßig über diese Berechtigung. Der einzige Teil der Sicherheits Beschreibung, der verwendet wird, ist der nicht geerbte Zugriffs Steuerungs Eintrag (ACE) in der freigegebenen Zugriffs Steuerungs Liste (DACL). Wenn Sie das **\_ containervererbungs** -Flag in den ACEs festlegen, wirkt sich die Sicherheits Beschreibung auf untergeordnete Namespaces aus. Sowohl Allow-als auch deny-ACEs sind zulässig.

> [!Note]  
> Da Deny-und allow-ACEs in einer DACL zulässig sind, ist die Reihenfolge der ACEs wichtig. Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

## <a name="syntax"></a>Syntax


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SD* \[ in\]
</dt> <dd>

Bytearray, das die Sicherheits Beschreibung bildet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **HRESULT** zurück, das den Status eines Methoden Aufrufes angibt. Für Skript-und Visual Basic Anwendungen kann das Ergebnis aus " [OutParameters. returnValue](parsing-outparameters-objects.md)" abgerufen werden. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

In der folgenden Liste sind die Rückgabewerte aufgelistet, die für " **-** ID" von Bedeutung sind.

<dl> <dt>

**S \_ OK**
</dt> <dd>

Die Methode wurde erfolgreich ausgeführt.

</dd> <dt>

**WBEM \_ E- \_ Zugriff \_ verweigert**
</dt> <dd>

Der Aufrufer verfügt nicht über ausreichende Rechte, um diese Methode aufzurufen.

</dd> <dt>

**WBEM \_ E- \_ Methode \_ deaktiviert**
</dt> <dd>

Es wurde versucht, diese Methode auf dem Betriebssystem auszuführen, das diese Methode nicht unterstützt.

</dd> <dt>

**ungültiges WBEM- \_ \_ \_ Objekt**
</dt> <dd>

Die SD übergibt keine grundlegenden Validierungstests.

</dd> <dt>

**\_Ungültiger WBEM E- \_ \_ Parameter**
</dt> <dd>

SD ist aufgrund einer der folgenden Aktionen ungültig:

-   DACL fehlt.
-   Die DACL ist ungültig.
-   Bei ACE ist das WBEM-Flag " **\_ Full \_ Write \_ Rep** " festgelegt, und der WBEM-Flag für **\_ partielle \_ Schreib \_** Vorgänge oder **WBEM- \_ Schreib \_ Anbieter** wurde nicht festgelegt.
-   Bei ACE ist **das \_ \_ ACE** -Flag "nur Erben" ohne das Flag " **Container \_ Vererbung \_** " festgelegt.
-   Der ACE hat ein unbekanntes Zugriffs Bit festgelegt.
-   ACE verfügt über ein Flag, das nicht in der Tabelle angezeigt wird.
-   ACE weist einen Typ auf, der nicht in der Tabelle ist.
-   Der Besitzer und die Gruppe fehlen in der SD.

Weitere Informationen zu den ACE-Flags (Access Control Entry) finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum programmgesteuerten oder manuellen Ändern der Namespace Sicherheit finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md).

## <a name="examples"></a>Beispiele

Das folgende Skript zeigt, wie Sie **sezd** verwenden, um die Namespace-Sicherheits Beschreibung für den Stamm Namespace festzulegen und in das Bytearray zu ändern, das in " *strausd*" angezeigt wird.


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



Im folgenden c#-Codebeispiel wird der System. Security. AccessControl. RawSecurityDescriptor verwendet, um neue CommonAce-Objekte in RawSecurityDescriptor. diskretionaryacl aufzulisten, einzufügen und zu entfernen und Sie dann wieder in ein Bytearray zu konvertieren, um Sie über sezd zu speichern. Ein SecurityIdentifier kann mithilfe von NTAccount abgerufen und übersetzt werden.


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: getd**](--systemsecurity-getsd.md)
</dt> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> </dl>

 

