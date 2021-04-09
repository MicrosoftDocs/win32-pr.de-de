---
description: Die Security- \_ Eigenschaft des Objekts "Swap-Locator" wird verwendet, um die Sicherheitseinstellungen für ein "Swap"-Objekt zu lesen oder festzulegen. Diese Eigenschaft ist ein Swap Security-Objekt.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755025"
---
# <a name="swbemlocatorsecurity_-property"></a><span data-ttu-id="f70c1-104">"Swap-Locator. Security"- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f70c1-104">SWbemLocator.Security\_ property</span></span>

<span data-ttu-id="f70c1-105">Die **Security \_** -Eigenschaft des Objekts " [**Swap-Locator**](swbemlocator.md) " wird verwendet, um die Sicherheitseinstellungen für ein " **Swap** "-Objekt zu lesen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f70c1-105">The **Security\_** property of the [**SWbemLocator**](swbemlocator.md) object is used to read or set the security settings for an **SWbemLocator** object.</span></span> <span data-ttu-id="f70c1-106">Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f70c1-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="f70c1-107">Das Festlegen **der \_ Security** -Eigenschaft eines " [**Swap**](swbemlocator.md) "-Objekts auf **null** gewährt allen Personen jederzeit uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="f70c1-107">Setting the **Security\_** property of an [**SWbemLocator**](swbemlocator.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="f70c1-108">Weitere Informationen finden Sie unter [**Swap Security**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="f70c1-108">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="f70c1-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f70c1-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f70c1-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f70c1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70c1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f70c1-111">Syntax</span></span>


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="f70c1-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f70c1-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f70c1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f70c1-113">Remarks</span></span>

<span data-ttu-id="f70c1-114">Die Eigenschaften eines " **taubemlocator. Security \_** "-Objekts haben keine Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="f70c1-114">The properties of an **SWbemLocator.Security\_** object have no default values.</span></span> <span data-ttu-id="f70c1-115">Wenn Sie versuchen, den Wert von " [**Swap Security. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) " oder " [**taubemsecurity. Identitäts ationlevel**](swbemsecurity-impersonationlevel.md) " für ein " [**taubemlocator**](swbemlocator.md) "-Objekt zu erhalten, bevor Sie es festgelegt haben, wird ein [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) -Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f70c1-115">If you attempt to get the value of [**SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) or [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on an [**SWbemLocator**](swbemlocator.md) object before you have set it, an [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) error results.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70c1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f70c1-116">Requirements</span></span>



| <span data-ttu-id="f70c1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f70c1-117">Requirement</span></span> | <span data-ttu-id="f70c1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f70c1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f70c1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f70c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f70c1-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f70c1-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f70c1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f70c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f70c1-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f70c1-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f70c1-123">Header</span><span class="sxs-lookup"><span data-stu-id="f70c1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f70c1-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f70c1-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f70c1-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f70c1-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="f70c1-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f70c1-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f70c1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f70c1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f70c1-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f70c1-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f70c1-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="f70c1-129">CLSID</span></span><br/>                    | <span data-ttu-id="f70c1-130">CLSID- \_ Austausch</span><span class="sxs-lookup"><span data-stu-id="f70c1-130">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="f70c1-131">IID</span><span class="sxs-lookup"><span data-stu-id="f70c1-131">IID</span></span><br/>                      | <span data-ttu-id="f70c1-132">IID \_ iswbemlocator</span><span class="sxs-lookup"><span data-stu-id="f70c1-132">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="f70c1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f70c1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70c1-134">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="f70c1-134">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="f70c1-135">Erstellen einer WMI-Anwendung oder eines Skripts</span><span class="sxs-lookup"><span data-stu-id="f70c1-135">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="f70c1-136">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="f70c1-136">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="f70c1-137">Festlegen der \_ Prozesssicherheit für Client Anwendungen \_</span><span class="sxs-lookup"><span data-stu-id="f70c1-137">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="f70c1-138">**Swap Security-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f70c1-138">**SWbemSecurity object**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="f70c1-139">Sichern einer Remote-WMI-Verbindung</span><span class="sxs-lookup"><span data-stu-id="f70c1-139">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




