---
description: 'WMI verfügt über Sicherheits Konstanten, die für die Überprüfung des Namespace Zugriffs durch \_ \_ SystemSecurity:: getcalleraccessrights verwendet werden.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Namespace-Zugriffsrechte Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041586"
---
# <a name="namespace-access-rights-constants"></a><span data-ttu-id="88486-103">Namespace-Zugriffsrechte Konstanten</span><span class="sxs-lookup"><span data-stu-id="88486-103">Namespace Access Rights Constants</span></span>

<span data-ttu-id="88486-104">WMI verfügt über Sicherheits Konstanten, die für die Überprüfung des Namespace Zugriffs durch [**\_ \_ SystemSecurity:: getcalleraccessrights**](--systemsecurity-getcalleraccessrights.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88486-104">WMI has security constants used for namespace access checking by [**\_\_SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span></span> <span data-ttu-id="88486-105">Sicherheitsinformationen zu Zugriffs Steuerungs Listen (ACLs, DACLs oder SACLs) finden Sie unter [Access Control Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [**Standard Zugriffsrechte**](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="88486-105">For security information about access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [**Standard Access Rights**](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="88486-106">Diese Konstanten werden in der **WBEM- \_ \_ sicherheitsflags** -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="88486-106">These constants are defined in the **WBEM\_SECURITY\_FLAGS** enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="88486-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM- \_ Aktivierung**</span><span class="sxs-lookup"><span data-stu-id="88486-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88486-108">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="88486-108">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="88486-109">Aktiviert das Konto und gewährt dem Benutzer Leseberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="88486-109">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="88486-110">Dies ist ein Standard Zugriffsrecht für alle Benutzer und entspricht der Berechtigung Konto aktivieren auf der Registerkarte Sicherheit des [*WMI-Steuer*](gloss-w.md)Elements.</span><span class="sxs-lookup"><span data-stu-id="88486-110">This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="88486-111">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="88486-111">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88486-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM- \_ Methode \_ Ausführen**</span><span class="sxs-lookup"><span data-stu-id="88486-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88486-113">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="88486-113">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="88486-114">Ermöglicht die Ausführung von-Methoden.</span><span class="sxs-lookup"><span data-stu-id="88486-114">Allows the execution of methods.</span></span> <span data-ttu-id="88486-115">Anbieter können zusätzliche Zugriffs Überprüfungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="88486-115">Providers can perform additional access checks.</span></span> <span data-ttu-id="88486-116">Dies ist ein Standard Zugriffsrecht für alle Benutzer und entspricht der Berechtigung Execute Methods auf der Registerkarte Sicherheit des WMI-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="88486-116">This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88486-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ Vollständiger \_ Schreibzugriff \_**</span><span class="sxs-lookup"><span data-stu-id="88486-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88486-118">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="88486-118">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="88486-119">Ermöglicht einem Benutzerkonto das Schreiben in Klassen im WMI-Repository und in-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="88486-119">Allows a user account to write to classes in the WMI repository as well as instances.</span></span> <span data-ttu-id="88486-120">Ein Benutzer kann nicht in System Klassen schreiben.</span><span class="sxs-lookup"><span data-stu-id="88486-120">A user cannot write to system classes.</span></span> <span data-ttu-id="88486-121">Nur Mitglieder der Gruppe "Administratoren" verfügen über diese Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="88486-121">Only members of the Administrators group have this permission.</span></span> <span data-ttu-id="88486-122">**WBEM \_ Voll \_ ständiger \_ Schreib** Zugriff entspricht der vollständigen Schreib Berechtigung auf der Registerkarte "Sicherheit" des WMI-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="88486-122">**WBEM\_FULL\_WRITE\_REP** corresponds to the Full Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88486-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_partieller \_ Schreibvorgang von WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="88486-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88486-124">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="88486-124">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="88486-125">Ermöglicht das Schreiben von Daten nur in-Instanzen, nicht in Klassen.</span><span class="sxs-lookup"><span data-stu-id="88486-125">Allows you to write data to instances only, not classes.</span></span> <span data-ttu-id="88486-126">Ein Benutzer kann keine Klassen in das [*WMI-Repository*](gloss-w.md)schreiben.</span><span class="sxs-lookup"><span data-stu-id="88486-126">A user cannot write classes to the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="88486-127">Nur Mitglieder der Gruppe "Administratoren" haben dieses Recht.</span><span class="sxs-lookup"><span data-stu-id="88486-127">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="88486-128">**WBEM \_ Partieller \_ Schreib \_** Zugriff entspricht der Berechtigung zum partiellen schreiben auf der Registerkarte Sicherheit des WMI-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="88486-128">**WBEM\_PARTIAL\_WRITE\_REP** corresponds to the Partial Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88486-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM- \_ Schreib \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="88486-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88486-130">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="88486-130">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="88486-131">Ermöglicht das Schreiben von Klassen und Instanzen in Anbieter.</span><span class="sxs-lookup"><span data-stu-id="88486-131">Allows writing classes and instances to providers.</span></span> <span data-ttu-id="88486-132">Beachten Sie, dass Anbieter bei der Identität eines Benutzers zusätzliche Zugriffs Überprüfungen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="88486-132">Note that providers can do additional access checks when impersonating a user.</span></span> <span data-ttu-id="88486-133">Dies ist ein Standard Zugriffsrecht für alle Benutzer und entspricht der Schreib Berechtigung des Anbieters auf der Registerkarte Sicherheit des WMI-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="88486-133">This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88486-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM- \_ Remote \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="88486-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88486-135">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="88486-135">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="88486-136">Ermöglicht einem Benutzerkonto das Remote Ausführen von Vorgängen, die von den oben beschriebenen Berechtigungen zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="88486-136">Allows a user account to remotely perform any operations allowed by the permissions described above.</span></span> <span data-ttu-id="88486-137">Nur Mitglieder der Gruppe "Administratoren" haben dieses Recht.</span><span class="sxs-lookup"><span data-stu-id="88486-137">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="88486-138">**WBEM \_ Der Remote \_ Zugriff** entspricht der Berechtigung Remote Aktivierung auf der Registerkarte Sicherheit des WMI-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="88486-138">**WBEM\_REMOTE\_ACCESS** corresponds to the Remote Enable permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88486-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88486-139">Requirements</span></span>



| <span data-ttu-id="88486-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88486-140">Requirement</span></span> | <span data-ttu-id="88486-141">Wert</span><span class="sxs-lookup"><span data-stu-id="88486-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="88486-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88486-142">Minimum supported client</span></span><br/> | <span data-ttu-id="88486-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88486-143">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="88486-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88486-144">Minimum supported server</span></span><br/> | <span data-ttu-id="88486-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88486-145">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="88486-146">Header</span><span class="sxs-lookup"><span data-stu-id="88486-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="88486-147"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="88486-147"><dt>Wbemcli.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88486-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88486-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88486-149">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="88486-149">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="88486-150">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="88486-150">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="88486-151">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="88486-151">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="88486-152">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="88486-152">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="88486-153">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="88486-153">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

