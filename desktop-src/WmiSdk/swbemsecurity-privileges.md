---
description: Die Privileges-Eigenschaft ist ein Objekt vom Typ"taubemprivilegeset". Diese Eigenschaft wird verwendet, um bestimmte Windows-Berechtigungen zu aktivieren oder zu deaktivieren. Möglicherweise müssen Sie eine dieser Berechtigungen festlegen, um bestimmte Aufgaben mithilfe der Windows-Verwaltungsinstrumentation (WMI)-API auszuführen.
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: "' Swap Security. Privileges '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215309"
---
# <a name="swbemsecurityprivileges-property"></a><span data-ttu-id="2606c-105">Swap Security. Privileges (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2606c-105">SWbemSecurity.Privileges property</span></span>

<span data-ttu-id="2606c-106">Die **Privileges** -Eigenschaft ist ein Objekt vom Typ" [**taubemprivilegeset**](swbemprivilegeset.md) ".</span><span class="sxs-lookup"><span data-stu-id="2606c-106">The **Privileges** property is an [**SWbemPrivilegeSet**](swbemprivilegeset.md) object.</span></span> <span data-ttu-id="2606c-107">Diese Eigenschaft wird verwendet, um bestimmte Windows-Berechtigungen zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2606c-107">This property is used to enable or disable specific Windows privileges.</span></span> <span data-ttu-id="2606c-108">Möglicherweise müssen Sie eine dieser Berechtigungen festlegen, um bestimmte Aufgaben mithilfe der Windows-Verwaltungsinstrumentation (WMI)-API auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2606c-108">You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.</span></span>

<span data-ttu-id="2606c-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2606c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="2606c-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2606c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2606c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2606c-111">Syntax</span></span>


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a><span data-ttu-id="2606c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2606c-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2606c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2606c-113">Remarks</span></span>

<span data-ttu-id="2606c-114">Diese Einstellung ermöglicht es Ihnen, Berechtigungen als Teil einer WMI-Monikerzeichenfolge zu erteilen oder aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="2606c-114">This setting allows you to grant or revoke privileges as part of a WMI moniker string.</span></span> <span data-ttu-id="2606c-115">Eine umfassende Liste der anwendbaren Werte finden Sie unter [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) und [**Berechtigungs Konstanten**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2606c-115">For the complete list of applicable values, see [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="2606c-116">Sie können die Berechtigungen für die Objekte " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbewbjectset**](swbemobjectset.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**taubemlocator**](swbemlocator.md) " ändern, indem Sie der Eigenschaft " **Privilegien** " [**die Objekte "**](swbemprivilege.md) ", ""</span><span class="sxs-lookup"><span data-stu-id="2606c-116">You can change the privileges defined for the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by adding [**SWbemPrivilege**](swbemprivilege.md) objects to the **Privileges** property.</span></span>

<span data-ttu-id="2606c-117">Es gibt wesentliche Unterschiede in der Art und Weise, in der verschiedene Versionen von Windows Änderungen an Berechtigungen behandeln.</span><span class="sxs-lookup"><span data-stu-id="2606c-117">There are fundamental differences in how different versions of Windows handle changes to privileges.</span></span> <span data-ttu-id="2606c-118">Wenn Sie eine Anwendung entwickeln, die nur auf Windows-Plattformen verwendet wird, können Sie Berechtigungen jederzeit festlegen oder widerrufen.</span><span class="sxs-lookup"><span data-stu-id="2606c-118">If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.</span></span>

<span data-ttu-id="2606c-119">Im folgenden Beispiel wird die **SeDebugPrivilege-Berechtigung** für die anfängliche monikerverbindung festgelegt, [**um ein-**](swbemservices.md) Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2606c-119">The following example sets the **SeDebugPrivilege** on the initial moniker connection to obtain an [**SWbemServices**](swbemservices.md) object.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



<span data-ttu-id="2606c-120">Weitere Informationen zum Formatieren der Sicherheits Zeichenfolge für eine monikerverbindung finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2606c-120">For more information about how to format the security string for a moniker connection, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="2606c-121">Im folgenden Beispiel wird dieselbe Aufgabe durchführt, die Berechtigung wird jedoch nach der anfänglichen Anmeldung bei WMI festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2606c-121">The following example performs the same task, but it sets the privilege after the initial log on to WMI.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



<span data-ttu-id="2606c-122">Beachten Sie, dass Sie bei Aufrufen von " [**taubemprivilegeset. addasstring**](swbemprivilegeset-addasstring.md)" den vollständigen Namen der Sicherheits Berechtigung verwenden müssen, z. b. "Setter", anstelle von "Debug".</span><span class="sxs-lookup"><span data-stu-id="2606c-122">Note that for calls to [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".</span></span>

## <a name="requirements"></a><span data-ttu-id="2606c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2606c-123">Requirements</span></span>



| <span data-ttu-id="2606c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2606c-124">Requirement</span></span> | <span data-ttu-id="2606c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2606c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2606c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2606c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2606c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2606c-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2606c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2606c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2606c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2606c-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2606c-130">Header</span><span class="sxs-lookup"><span data-stu-id="2606c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2606c-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2606c-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2606c-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2606c-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="2606c-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2606c-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2606c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2606c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2606c-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2606c-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2606c-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="2606c-136">CLSID</span></span><br/>                    | <span data-ttu-id="2606c-137">CLSID- \_ Swap-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="2606c-137">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="2606c-138">IID</span><span class="sxs-lookup"><span data-stu-id="2606c-138">IID</span></span><br/>                      | <span data-ttu-id="2606c-139">IID \_ iswbemsecurity</span><span class="sxs-lookup"><span data-stu-id="2606c-139">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="2606c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2606c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2606c-141">**Austausch Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="2606c-141">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="2606c-142">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="2606c-142">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="2606c-143">**Swap-Privileg**</span><span class="sxs-lookup"><span data-stu-id="2606c-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> </dl>

 

 




