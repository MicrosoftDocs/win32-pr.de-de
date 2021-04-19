---
description: Die Security- \_ Eigenschaft des errbewbjectset-Objekts wird verwendet, um die Sicherheitseinstellungen für ein errbewbjectset-Objekt zu erhalten oder festzulegen. Diese Eigenschaft ist ein Swap Security-Objekt.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: SWbemObjectSet.Security_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348523"
---
# <a name="swbemobjectsetsecurity_-property"></a><span data-ttu-id="61cb3-104">Errbemubjectset. Security- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="61cb3-104">SWbemObjectSet.Security\_ property</span></span>

<span data-ttu-id="61cb3-105">Die **Security \_** -Eigenschaft des [**errbewbjectset**](swbemobjectset.md) -Objekts wird verwendet, um die Sicherheitseinstellungen für ein **errbewbjectset** -Objekt zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="61cb3-105">The **Security\_** property of the [**SWbemObjectSet**](swbemobjectset.md) object is used to get or set the security settings for an **SWbemObjectSet** object.</span></span> <span data-ttu-id="61cb3-106">Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="61cb3-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="61cb3-107">Das Festlegen [**der \_ Security**](swbemobject-security-.md) -Eigenschaft eines ' [**errbemubjectset**](swbemobjectset.md) '-Objekts auf **null** gewährt allen Benutzern jederzeit uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="61cb3-107">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectSet**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="61cb3-108">Weitere Informationen zu den Auswirkungen des unbegrenzten Zugriffs finden Sie unter [**Swap Security**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="61cb3-108">For more information about the implications of unlimited access, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="61cb3-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="61cb3-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="61cb3-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="61cb3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cb3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="61cb3-111">Syntax</span></span>


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="61cb3-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="61cb3-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="61cb3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61cb3-113">Requirements</span></span>



| <span data-ttu-id="61cb3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61cb3-114">Requirement</span></span> | <span data-ttu-id="61cb3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="61cb3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61cb3-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61cb3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61cb3-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61cb3-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61cb3-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61cb3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61cb3-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61cb3-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61cb3-120">Header</span><span class="sxs-lookup"><span data-stu-id="61cb3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61cb3-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="61cb3-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="61cb3-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="61cb3-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="61cb3-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="61cb3-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="61cb3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="61cb3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61cb3-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61cb3-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="61cb3-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="61cb3-126">CLSID</span></span><br/>                    | <span data-ttu-id="61cb3-127">CLSID- \_ Swap-Objekt Satz</span><span class="sxs-lookup"><span data-stu-id="61cb3-127">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="61cb3-128">IID</span><span class="sxs-lookup"><span data-stu-id="61cb3-128">IID</span></span><br/>                      | <span data-ttu-id="61cb3-129">IID \_ iswbemubjectset</span><span class="sxs-lookup"><span data-stu-id="61cb3-129">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="61cb3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61cb3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cb3-131">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="61cb3-131">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="61cb3-132">Erstellen einer WMI-Anwendung oder eines Skripts</span><span class="sxs-lookup"><span data-stu-id="61cb3-132">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="61cb3-133">Sichern von Skript Clients</span><span class="sxs-lookup"><span data-stu-id="61cb3-133">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 




