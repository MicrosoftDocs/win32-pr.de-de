---
description: Die Security- \_ Eigenschaft des-Objekts mit dem-Objekt wird zum Lesen oder Festlegen der Sicherheitseinstellungen für ein-Objekt vom typaustausch verwendet.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: SWbemObject.Security_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349219"
---
# <a name="swbemobjectsecurity_-property"></a><span data-ttu-id="f25a8-103">Errbemubject. Security ( \_ Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f25a8-103">SWbemObject.Security\_ property</span></span>

<span data-ttu-id="f25a8-104">Die **Security \_** -Eigenschaft des [**-Objekts mit**](swbemobject.md) dem-Objekt wird zum Lesen oder Festlegen der Sicherheitseinstellungen für ein-Objekt vom **typaustausch** verwendet.</span><span class="sxs-lookup"><span data-stu-id="f25a8-104">The **Security\_** property of the [**SWbemObject**](swbemobject.md) object is used to read, or set the security settings for an **SWbemObject** object.</span></span> <span data-ttu-id="f25a8-105">Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f25a8-105">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="f25a8-106">Die Sicherheitseinstellungen in diesem Objekt geben nicht die Authentifizierung, den Identitätswechsel oder die Berechtigungseinstellungen an, die für eine Verbindung mit Windows-Verwaltungsinstrumentation (WMI) vorgenommen wurden, oder die für den Proxy geltenden Sicherheit, wenn ein Objekt in einem asynchronen-Befehl an eine Senke übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f25a8-106">The security settings in this object do not indicate the authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="f25a8-107">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="f25a8-107">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

> [!Note]  
> <span data-ttu-id="f25a8-108">Das Festlegen **der \_ Security** -Eigenschaft eines " [**errbemubject**](swbemobject.md) "-Objekts auf **null** gewährt allen Benutzern uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="f25a8-108">Setting the **Security\_** property of an [**SWbemObject**](swbemobject.md) object to **NULL** grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="f25a8-109">Weitere Informationen finden Sie unter [**Swap Security**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="f25a8-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="f25a8-110">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f25a8-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f25a8-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f25a8-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f25a8-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f25a8-112">Syntax</span></span>


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="f25a8-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f25a8-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="f25a8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f25a8-114">Requirements</span></span>



| <span data-ttu-id="f25a8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f25a8-115">Requirement</span></span> | <span data-ttu-id="f25a8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f25a8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f25a8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f25a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f25a8-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f25a8-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f25a8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f25a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f25a8-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f25a8-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f25a8-121">Header</span><span class="sxs-lookup"><span data-stu-id="f25a8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f25a8-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f25a8-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f25a8-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f25a8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f25a8-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f25a8-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f25a8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f25a8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f25a8-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f25a8-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f25a8-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="f25a8-127">CLSID</span></span><br/>                    | <span data-ttu-id="f25a8-128">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="f25a8-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f25a8-129">IID</span><span class="sxs-lookup"><span data-stu-id="f25a8-129">IID</span></span><br/>                      | <span data-ttu-id="f25a8-130">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="f25a8-130">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f25a8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f25a8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25a8-132">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="f25a8-132">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f25a8-133">Erstellen einer WMI-Anwendung oder eines Skripts</span><span class="sxs-lookup"><span data-stu-id="f25a8-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="f25a8-134">Festlegen der \_ Prozesssicherheit für Client Anwendungen \_</span><span class="sxs-lookup"><span data-stu-id="f25a8-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="f25a8-135">**Austausch Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="f25a8-135">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="f25a8-136">**Wbemauthenticationlevelerum**</span><span class="sxs-lookup"><span data-stu-id="f25a8-136">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="f25a8-137">**Wbemimpersonationlevelenum**</span><span class="sxs-lookup"><span data-stu-id="f25a8-137">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="f25a8-138">**Wbemprivilegeumum**</span><span class="sxs-lookup"><span data-stu-id="f25a8-138">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="f25a8-139">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="f25a8-139">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




