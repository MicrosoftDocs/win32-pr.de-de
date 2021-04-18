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
# <a name="setsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="f5d09-105">Die Methode "-Methode" der \_ \_ Klasse "System Security"</span><span class="sxs-lookup"><span data-stu-id="f5d09-105">SetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="f5d09-106">Die **sezd-** Methode legt die Sicherheits Beschreibung für den Namespace fest, mit dem ein Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f5d09-106">The **SetSD** method sets the security descriptor for the namespace to which a user is connected.</span></span> <span data-ttu-id="f5d09-107">Diese Methode erfordert eine Sicherheits Beschreibung im Format des binären Byte Arrays.</span><span class="sxs-lookup"><span data-stu-id="f5d09-107">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="f5d09-108">Wenn Sie ein Skript schreiben, verwenden Sie die [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f5d09-108">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span> <span data-ttu-id="f5d09-109">Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f5d09-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="f5d09-110">Wenn Sie in C++ programmieren, können Sie den binären Sicherheits Deskriptor mithilfe von [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und die Konvertierungs Methoden [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f5d09-110">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="f5d09-111">Ein Benutzer muss über die Berechtigung zum **Schreiben von \_ DAC** verfügen, und ein Administrator verfügt standardmäßig über diese Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="f5d09-111">A user must have the **WRITE\_DAC** permission, and by default, an administrator has that permission.</span></span> <span data-ttu-id="f5d09-112">Der einzige Teil der Sicherheits Beschreibung, der verwendet wird, ist der nicht geerbte Zugriffs Steuerungs Eintrag (ACE) in der freigegebenen Zugriffs Steuerungs Liste (DACL).</span><span class="sxs-lookup"><span data-stu-id="f5d09-112">The only part of the security descriptor that is used is the noninherited access control entry (ACE) in the discretionary access control list (DACL).</span></span> <span data-ttu-id="f5d09-113">Wenn Sie das **\_ containervererbungs** -Flag in den ACEs festlegen, wirkt sich die Sicherheits Beschreibung auf untergeordnete Namespaces aus.</span><span class="sxs-lookup"><span data-stu-id="f5d09-113">By setting the **CONTAINER\_INHERIT** flag in the ACEs, the security descriptor affects child namespaces.</span></span> <span data-ttu-id="f5d09-114">Sowohl Allow-als auch deny-ACEs sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="f5d09-114">Both allow and deny ACEs are permitted.</span></span>

> [!Note]  
> <span data-ttu-id="f5d09-115">Da Deny-und allow-ACEs in einer DACL zulässig sind, ist die Reihenfolge der ACEs wichtig.</span><span class="sxs-lookup"><span data-stu-id="f5d09-115">Because deny and allow ACEs are both permitted in a DACL, the order of ACEs is important.</span></span> <span data-ttu-id="f5d09-116">Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="f5d09-116">For more information, see [Ordering of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f5d09-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5d09-117">Syntax</span></span>


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="f5d09-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5d09-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d09-119">*SD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5d09-119">*SD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d09-120">Bytearray, das die Sicherheits Beschreibung bildet.</span><span class="sxs-lookup"><span data-stu-id="f5d09-120">Byte array that makes up the security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d09-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5d09-121">Return value</span></span>

<span data-ttu-id="f5d09-122">Gibt ein **HRESULT** zurück, das den Status eines Methoden Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="f5d09-122">Returns an **HRESULT** that indicates the status of a method call.</span></span> <span data-ttu-id="f5d09-123">Für Skript-und Visual Basic Anwendungen kann das Ergebnis aus " [OutParameters. returnValue](parsing-outparameters-objects.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f5d09-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="f5d09-124">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f5d09-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="f5d09-125">In der folgenden Liste sind die Rückgabewerte aufgelistet, die für " **-** ID" von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="f5d09-125">The following list lists the return values that are significant to **SetSD**.</span></span>

<dl> <dt>

<span data-ttu-id="f5d09-126">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="f5d09-126">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="f5d09-127">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5d09-127">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="f5d09-128">**WBEM \_ E- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="f5d09-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="f5d09-129">Der Aufrufer verfügt nicht über ausreichende Rechte, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5d09-129">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="f5d09-130">**WBEM \_ E- \_ Methode \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="f5d09-130">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="f5d09-131">Es wurde versucht, diese Methode auf dem Betriebssystem auszuführen, das diese Methode nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5d09-131">Attempted to run this method on OS that does not support it.</span></span>

</dd> <dt>

<span data-ttu-id="f5d09-132">**ungültiges WBEM- \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="f5d09-132">**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="f5d09-133">Die SD übergibt keine grundlegenden Validierungstests.</span><span class="sxs-lookup"><span data-stu-id="f5d09-133">SD does not pass basic validity tests.</span></span>

</dd> <dt>

<span data-ttu-id="f5d09-134">**\_Ungültiger WBEM E- \_ \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="f5d09-134">**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="f5d09-135">SD ist aufgrund einer der folgenden Aktionen ungültig:</span><span class="sxs-lookup"><span data-stu-id="f5d09-135">SD is not valid due to one of the following:</span></span>

-   <span data-ttu-id="f5d09-136">DACL fehlt.</span><span class="sxs-lookup"><span data-stu-id="f5d09-136">DACL is missing.</span></span>
-   <span data-ttu-id="f5d09-137">Die DACL ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f5d09-137">DACL is not valid.</span></span>
-   <span data-ttu-id="f5d09-138">Bei ACE ist das WBEM-Flag " **\_ Full \_ Write \_ Rep** " festgelegt, und der WBEM-Flag für **\_ partielle \_ Schreib \_** Vorgänge oder **WBEM- \_ Schreib \_ Anbieter** wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5d09-138">ACE has the **WBEM\_FULL\_WRITE\_REP** flag set, and the **WBEM\_PARTIAL\_WRITE\_REP** or **WBEM\_WRITE\_PROVIDER** flag is not set.</span></span>
-   <span data-ttu-id="f5d09-139">Bei ACE ist **das \_ \_ ACE** -Flag "nur Erben" ohne das Flag " **Container \_ Vererbung \_** " festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5d09-139">ACE has the **INHERIT\_ONLY\_ACE** flag set without the **CONTAINER\_INHERIT\_ACE** flag.</span></span>
-   <span data-ttu-id="f5d09-140">Der ACE hat ein unbekanntes Zugriffs Bit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5d09-140">ACE has an unknown access bit set.</span></span>
-   <span data-ttu-id="f5d09-141">ACE verfügt über ein Flag, das nicht in der Tabelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f5d09-141">ACE has a flag set that is not in the table.</span></span>
-   <span data-ttu-id="f5d09-142">ACE weist einen Typ auf, der nicht in der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="f5d09-142">ACE has a type that is not in the table.</span></span>
-   <span data-ttu-id="f5d09-143">Der Besitzer und die Gruppe fehlen in der SD.</span><span class="sxs-lookup"><span data-stu-id="f5d09-143">The owner and group are missing from the SD.</span></span>

<span data-ttu-id="f5d09-144">Weitere Informationen zu den ACE-Flags (Access Control Entry) finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f5d09-144">For more information about the access control entry (ACE) flags, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5d09-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5d09-145">Remarks</span></span>

<span data-ttu-id="f5d09-146">Weitere Informationen zum programmgesteuerten oder manuellen Ändern der Namespace Sicherheit finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="f5d09-146">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f5d09-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5d09-147">Examples</span></span>

<span data-ttu-id="f5d09-148">Das folgende Skript zeigt, wie Sie **sezd** verwenden, um die Namespace-Sicherheits Beschreibung für den Stamm Namespace festzulegen und in das Bytearray zu ändern, das in " *strausd*" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f5d09-148">The following script shows how to use **SetSD** to set the namespace security descriptor for the root namespace and change it to the byte array shown in *strSD*.</span></span>


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



<span data-ttu-id="f5d09-149">Im folgenden c#-Codebeispiel wird der System. Security. AccessControl. RawSecurityDescriptor verwendet, um neue CommonAce-Objekte in RawSecurityDescriptor. diskretionaryacl aufzulisten, einzufügen und zu entfernen und Sie dann wieder in ein Bytearray zu konvertieren, um Sie über sezd zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f5d09-149">The following C# code sample uses the System.Security.AccessControl.RawSecurityDescriptor to enumerate, insert and remove new CommonAce objects in RawSecurityDescriptor.DiscretionaryAcl and then convert it back to an byte array to save it via SetSD.</span></span> <span data-ttu-id="f5d09-150">Ein SecurityIdentifier kann mithilfe von NTAccount abgerufen und übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f5d09-150">An SecurityIdentifier can be retrieved by using NTAccount and Translate.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f5d09-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5d09-151">Requirements</span></span>



| <span data-ttu-id="f5d09-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5d09-152">Requirement</span></span> | <span data-ttu-id="f5d09-153">Wert</span><span class="sxs-lookup"><span data-stu-id="f5d09-153">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f5d09-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5d09-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d09-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5d09-155">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f5d09-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5d09-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d09-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5d09-157">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f5d09-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5d09-158">Namespace</span></span><br/>                | <span data-ttu-id="f5d09-159">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="f5d09-159">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f5d09-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5d09-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d09-161">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="f5d09-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f5d09-162">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="f5d09-162">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="f5d09-163">**\_\_SystemSecurity:: getd**</span><span class="sxs-lookup"><span data-stu-id="f5d09-163">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="f5d09-164">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="f5d09-164">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="f5d09-165">**Win32- \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="f5d09-165">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="f5d09-166">**Win32- \_ securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f5d09-166">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="f5d09-167">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="f5d09-167">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

