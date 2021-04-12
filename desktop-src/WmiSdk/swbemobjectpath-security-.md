---
description: Die Security-Eigenschaft des Objekts "errbewbjectpath" wird verwendet, um die Sicherheitskomponenten eines Objekt Pfads zu erhalten oder festzulegen.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215317"
---
# <a name="swbemobjectpathsecurity_-property"></a><span data-ttu-id="14a8b-103">Errbemubjectpath. Security- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14a8b-103">SWbemObjectPath.Security\_ property</span></span>

<span data-ttu-id="14a8b-104">Die **Security** -Eigenschaft des Objekts " [**errbewbjectpath**](swbemobjectpath.md) " wird verwendet, um die Sicherheitskomponenten eines Objekt Pfads zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="14a8b-104">The **Security** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is used to get or set the security components of an object path.</span></span> <span data-ttu-id="14a8b-105">Beachten Sie, dass es nicht verwendet wird, um Sicherheits Attribute des Objekts " **errbemubjectpath** " selbst festzulegen.</span><span class="sxs-lookup"><span data-stu-id="14a8b-105">Note that it is not used to set security attributes of the **SWbemObjectPath** object itself.</span></span> <span data-ttu-id="14a8b-106">Sie wird nur verwendet, um die Sicherheitskomponenten des Pfads für ein Objekt vom Typ " [**Swap**](swbemlocator.md) " darzustellen.</span><span class="sxs-lookup"><span data-stu-id="14a8b-106">It is used only to represent the security components of the path for an [**SWbemLocator**](swbemlocator.md) object.</span></span> <span data-ttu-id="14a8b-107">Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="14a8b-107">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="14a8b-108">Durch das Festlegen der [**\_ Sicherheits**](swbemobject-security-.md) Eigenschaft eines " [**errbemubjectpath**](swbemobjectset.md) "-Objekts auf **null** wird allen Benutzern jederzeit uneingeschränkter Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="14a8b-108">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectPath**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="14a8b-109">Weitere Informationen finden Sie unter [**Swap Security**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="14a8b-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="14a8b-110">Weitere Informationen finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="14a8b-110">For more information, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="14a8b-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="14a8b-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a8b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="14a8b-112">Syntax</span></span>


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="14a8b-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="14a8b-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="14a8b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14a8b-114">Requirements</span></span>



| <span data-ttu-id="14a8b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14a8b-115">Requirement</span></span> | <span data-ttu-id="14a8b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="14a8b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14a8b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14a8b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14a8b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14a8b-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14a8b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14a8b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14a8b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14a8b-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14a8b-121">Header</span><span class="sxs-lookup"><span data-stu-id="14a8b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14a8b-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="14a8b-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="14a8b-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="14a8b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="14a8b-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="14a8b-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="14a8b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14a8b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14a8b-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14a8b-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="14a8b-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="14a8b-127">CLSID</span></span><br/>                    | <span data-ttu-id="14a8b-128">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="14a8b-128">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="14a8b-129">IID</span><span class="sxs-lookup"><span data-stu-id="14a8b-129">IID</span></span><br/>                      | <span data-ttu-id="14a8b-130">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="14a8b-130">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="14a8b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14a8b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a8b-132">**Errbemubjectpath**</span><span class="sxs-lookup"><span data-stu-id="14a8b-132">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> <dt>

[<span data-ttu-id="14a8b-133">Erstellen einer WMI-Anwendung oder eines Skripts</span><span class="sxs-lookup"><span data-stu-id="14a8b-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="14a8b-134">Festlegen der \_ Prozesssicherheit für Client Anwendungen \_</span><span class="sxs-lookup"><span data-stu-id="14a8b-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> </dl>

 

 




