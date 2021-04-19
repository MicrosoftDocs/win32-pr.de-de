---
description: Ruft die Sicherheits Beschreibung für den Namespace ab, mit dem der Benutzer verbunden ist. Diese Methode gibt eine Sicherheits Beschreibung im Format des binären Byte Arrays zurück. Wenn Sie ein Skript schreiben, verwenden Sie die getsecuritydescriptor-Methode.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Gezd-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360588"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="94f85-105">Gezd-Methode der \_ \_ System Security-Klasse</span><span class="sxs-lookup"><span data-stu-id="94f85-105">GetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="94f85-106">Die **gezd-** Methode ruft die Sicherheits Beschreibung für den Namespace ab, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="94f85-106">The **GetSD** method gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="94f85-107">Diese Methode gibt eine Sicherheits Beschreibung im Format des binären Byte Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="94f85-107">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="94f85-108">Wenn Sie ein Skript schreiben, verwenden Sie die [**getsecuritydescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="94f85-108">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span> <span data-ttu-id="94f85-109">Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="94f85-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="94f85-110">Der Benutzer muss über die Berechtigung zum **Lesen von \_ Steuer** Elementen verfügen.</span><span class="sxs-lookup"><span data-stu-id="94f85-110">The user must have the **READ\_CONTROL** permission.</span></span> <span data-ttu-id="94f85-111">Standardmäßig verfügen Administratoren über diese Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="94f85-111">By default, administrators have that permission.</span></span> <span data-ttu-id="94f85-112">Der einzige Teil der Sicherheits Beschreibung, die tatsächlich verwendet wird, ist die freigegebene Zugriffs Steuerungs Liste (DACL).</span><span class="sxs-lookup"><span data-stu-id="94f85-112">The only part of the security descriptor that is actually used is the discretionary access control list (DACL).</span></span> <span data-ttu-id="94f85-113">Die DACL kann sowohl geerbte als auch nicht geerbte ACEs enthalten.</span><span class="sxs-lookup"><span data-stu-id="94f85-113">The DACL can contain both inherited and non-inherited ACEs.</span></span> <span data-ttu-id="94f85-114">Deny-und allow-ACEs sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="94f85-114">Both deny and allow ACEs are permitted.</span></span>

<span data-ttu-id="94f85-115">Wenn Sie in C++ programmieren, können Sie den binären Sicherheits Deskriptor mithilfe von [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und die Konvertierungs Methoden [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="94f85-115">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

## <a name="syntax"></a><span data-ttu-id="94f85-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f85-116">Syntax</span></span>


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="94f85-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="94f85-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f85-118">*SD* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="94f85-118">*SD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94f85-119">Sicherheits Beschreibung im Format des binären Byte Arrays.</span><span class="sxs-lookup"><span data-stu-id="94f85-119">Security descriptor in binary byte array format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f85-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94f85-120">Return value</span></span>

<span data-ttu-id="94f85-121">Diese Methode gibt ein **HRESULT** zurück, das den Status des Methoden Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="94f85-121">This method returns an **HRESULT** indicating the status of the method call.</span></span> <span data-ttu-id="94f85-122">In der folgenden Liste sind die Rückgabewerte aufgelistet, die für **ge-d** von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="94f85-122">The following list lists the return values that are of significance to **GetSD**.</span></span> <span data-ttu-id="94f85-123">Für Skript-und Visual Basic Anwendungen kann das Ergebnis aus " [OutParameters. returnValue](parsing-outparameters-objects.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="94f85-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="94f85-124">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="94f85-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="94f85-125">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="94f85-125">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="94f85-126">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94f85-126">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="94f85-127">**WBEM \_ E- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="94f85-127">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="94f85-128">Der Aufrufer verfügt nicht über ausreichende Rechte, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="94f85-128">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="94f85-129">**WBEM \_ E- \_ Methode \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="94f85-129">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="94f85-130">Es wurde versucht, diese Methode auf einem nicht unterstützten System auszuführen.</span><span class="sxs-lookup"><span data-stu-id="94f85-130">Attempted to run this method on an unsupported system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94f85-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94f85-131">Remarks</span></span>

<span data-ttu-id="94f85-132">Weitere Informationen zum programmgesteuerten oder manuellen Ändern der Namespace Sicherheit finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="94f85-132">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="94f85-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94f85-133">Examples</span></span>

<span data-ttu-id="94f85-134">Das folgende Skript zeigt, wie Sie **getd** verwenden, um die aktuelle Sicherheits Beschreibung für den root \\ Cimv2-Namespace abzurufen und in das Bytearray zu ändern, das in **displaysd** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="94f85-134">The following script shows you how to use **GetSD** to obtain the current security descriptor for the Root\\Cimv2 namespace and change it to the byte array shown in **DisplaySD**.</span></span>


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a><span data-ttu-id="94f85-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94f85-135">Requirements</span></span>



| <span data-ttu-id="94f85-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94f85-136">Requirement</span></span> | <span data-ttu-id="94f85-137">Wert</span><span class="sxs-lookup"><span data-stu-id="94f85-137">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="94f85-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94f85-138">Minimum supported client</span></span><br/> | <span data-ttu-id="94f85-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94f85-139">Windows Vista</span></span><br/>       |
| <span data-ttu-id="94f85-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94f85-140">Minimum supported server</span></span><br/> | <span data-ttu-id="94f85-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94f85-141">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="94f85-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="94f85-142">Namespace</span></span><br/>                | <span data-ttu-id="94f85-143">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="94f85-143">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="94f85-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94f85-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f85-145">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="94f85-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="94f85-146">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="94f85-146">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="94f85-147">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="94f85-147">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="94f85-148">**Win32- \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="94f85-148">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="94f85-149">**\_\_SystemSecurity::-ID**</span><span class="sxs-lookup"><span data-stu-id="94f85-149">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="94f85-150">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94f85-150">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="94f85-151">**Win32- \_ securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="94f85-151">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="94f85-152">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="94f85-152">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

