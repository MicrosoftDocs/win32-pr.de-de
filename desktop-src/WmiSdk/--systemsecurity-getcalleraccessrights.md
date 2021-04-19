---
description: Legt den rights-Parameter als Bitmap fest, wobei jedes Bit einem Zugriffsrecht entspricht.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Getcalleraccessrights-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353852"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a><span data-ttu-id="57ad3-103">Getcalleraccessrights-Methode der \_ \_ System Security-Klasse</span><span class="sxs-lookup"><span data-stu-id="57ad3-103">GetCallerAccessRights method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="57ad3-104">Die **\_ \_ SystemSecurity:: getcalleraccessrights** -Methode legt den *Rights* -Parameter als Bitmap fest, wobei jedes Bit einem Zugriffsrecht entspricht.</span><span class="sxs-lookup"><span data-stu-id="57ad3-104">The **\_\_SystemSecurity::GetCallerAccessRights** method sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span> <span data-ttu-id="57ad3-105">Jeder Client kann diesen Befehl zum Bestimmen der Rechte des Clients abrufen.</span><span class="sxs-lookup"><span data-stu-id="57ad3-105">Any client can call this to determine which rights the client has.</span></span> <span data-ttu-id="57ad3-106">Diese Methode ist nützlich für Clients, die Features aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="57ad3-106">This method is useful for clients that enable or disable features.</span></span> <span data-ttu-id="57ad3-107">Beispielsweise kann eine GUI-Anwendung eine Schaltfläche deaktivieren, wenn der aktuell angemeldete Benutzer nicht über Methoden Ausführungsrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="57ad3-107">For example, a GUI application might disable a button if the currently logged-on user does not have method execution rights.</span></span>

<span data-ttu-id="57ad3-108">Jeder aktivierte Client hat das Recht, **getcalleraccessrights** aufzurufen, auch wenn dieser Client nicht über allgemeine Methoden Ausführungsrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="57ad3-108">Any enabled client has the right to call **GetCallerAccessRights**, even if that client does not have general method execution rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ad3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="57ad3-109">Syntax</span></span>


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a><span data-ttu-id="57ad3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="57ad3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ad3-111">*Rechte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57ad3-111">*rights* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57ad3-112">Zugriffsrechte des Clients.</span><span class="sxs-lookup"><span data-stu-id="57ad3-112">Access rights of the client.</span></span> <span data-ttu-id="57ad3-113">Weitere Informationen finden Sie unter [**\_ \_ SystemSecurity**](--systemsecurity.md) und [WMI-Sicherheits Konstanten](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="57ad3-113">For more information, see [**\_\_SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span></span>

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span data-ttu-id="57ad3-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ Aktivieren** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="57ad3-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-115">Aktiviert das Konto und gewährt dem Benutzer Leseberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="57ad3-115">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="57ad3-116">Dies ist das Standard Zugriffsrecht für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="57ad3-116">This is the default access right for all users.</span></span>

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span data-ttu-id="57ad3-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ Methode \_ Execute** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="57ad3-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-118">Ermöglicht die Ausführung von-Methoden.</span><span class="sxs-lookup"><span data-stu-id="57ad3-118">Allows the execution of methods.</span></span>

> [!Note]  
> <span data-ttu-id="57ad3-119">Anbieter können zusätzliche Zugriffs Überprüfungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="57ad3-119">Providers may perform additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span data-ttu-id="57ad3-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ Vollständiger \_ Schreib \_** Zugriff (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="57ad3-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-121">Ermöglicht es dem Aufrufer, dem Sicherheitskontext oder dem Benutzer, in Klassen und Instanzen mit Ausnahme von System Klassen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="57ad3-121">Allows the caller, security context, or user to write to classes and instances except for system classes.</span></span>

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span data-ttu-id="57ad3-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ Partieller \_ Schreib \_ Rep** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="57ad3-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-123">Ermöglicht dem Aufrufer, dem Sicherheitskontext oder dem Benutzer das Schreiben von Anbieter Instanzen, aber nicht von statischen Klassen oder statischen Instanzen in das Repository.</span><span class="sxs-lookup"><span data-stu-id="57ad3-123">Allows the caller, security context, or user to write provider instances but not static classes or static instances to the repository.</span></span>

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span data-ttu-id="57ad3-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ Schreib \_ Anbieter** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="57ad3-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-125">Ermöglicht dem Aufrufer, dem Sicherheitskontext oder dem Benutzer das Schreiben von Klassen und Instanzen in Anbieter.</span><span class="sxs-lookup"><span data-stu-id="57ad3-125">Allows the caller, security context, or user to write classes and instances to providers.</span></span>

> [!Note]  
> <span data-ttu-id="57ad3-126">Die Identitätswechsel von Anbietern können zusätzliche Zugriffs Überprüfungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="57ad3-126">Impersonating providers may do additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span data-ttu-id="57ad3-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ Remote \_ Zugriff** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="57ad3-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-128">Ermöglicht einem Benutzerkonto das Remote Ausführen von Vorgängen, die von den von anderen Bits festgelegten Berechtigungen zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="57ad3-128">Allows a user account to remotely perform any operations allowed by the permissions set by other bits.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="57ad3-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="57ad3-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-130">Ermöglicht den Lesezugriff auf die Sicherheits Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="57ad3-130">Allows read access to the security descriptors.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="57ad3-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="57ad3-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="57ad3-132">Ermöglicht den Schreibzugriff auf freigegebene Zugriffs Steuerungs Listen (DACL).</span><span class="sxs-lookup"><span data-stu-id="57ad3-132">Allows write access to discretionary access control lists (DACL).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ad3-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57ad3-133">Return value</span></span>

<span data-ttu-id="57ad3-134">Diese Methode gibt ein **HRESULT** zurück, das den Status des Methoden Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="57ad3-134">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="57ad3-135">In der folgenden Liste sind die Rückgabewerte aufgelistet, die für [**Set9XUserList**](--systemsecurity-set9xuserlist.md)von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="57ad3-135">The following list lists the return values that are of significance to [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span></span> <span data-ttu-id="57ad3-136">Für Skript-und Visual Basic Anwendungen kann das Ergebnis aus " [OutParameters. returnValue](parsing-outparameters-objects.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="57ad3-136">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="57ad3-137">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="57ad3-137">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="57ad3-138">**WBEM \_ E- \_ Methode \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="57ad3-138">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="57ad3-139">Diese Methode wird auf unterstützten Versionen von Windows nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="57ad3-139">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57ad3-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57ad3-140">Requirements</span></span>



| <span data-ttu-id="57ad3-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57ad3-141">Requirement</span></span> | <span data-ttu-id="57ad3-142">Wert</span><span class="sxs-lookup"><span data-stu-id="57ad3-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="57ad3-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57ad3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="57ad3-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ad3-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="57ad3-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57ad3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="57ad3-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57ad3-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="57ad3-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="57ad3-147">Namespace</span></span><br/>                | <span data-ttu-id="57ad3-148">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="57ad3-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="57ad3-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57ad3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ad3-150">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="57ad3-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="57ad3-151">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="57ad3-151">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="57ad3-152">**\_\_SystemSecurity:: getd**</span><span class="sxs-lookup"><span data-stu-id="57ad3-152">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="57ad3-153">**\_\_SystemSecurity::-ID**</span><span class="sxs-lookup"><span data-stu-id="57ad3-153">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="57ad3-154">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="57ad3-154">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="57ad3-155">**Win32- \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="57ad3-155">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="57ad3-156">**Win32- \_ securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="57ad3-156">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="57ad3-157">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="57ad3-157">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

<span data-ttu-id="57ad3-158">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="57ad3-158">WMI Security Constants</span></span>
</dt> </dl>

 

