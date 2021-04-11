---
description: Die Name-Eigenschaft eines "taubemprivilege"-Objekts ist eine Zeichenfolge, die eine Berechtigung eindeutig beschreibt.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: SWbemPrivilege.Name-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218293"
---
# <a name="swbemprivilegename-property"></a><span data-ttu-id="49901-103">SWbemPrivilege.Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="49901-103">SWbemPrivilege.Name property</span></span>

<span data-ttu-id="49901-104">Die **Name** -Eigenschaft eines " [**taubemprivilege**](swbemprivilege.md) "-Objekts ist eine Zeichenfolge, die eine Berechtigung eindeutig beschreibt.</span><span class="sxs-lookup"><span data-stu-id="49901-104">The **Name** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that uniquely describes a privilege.</span></span> <span data-ttu-id="49901-105">Beispielsweise hat die Berechtigung, die steuert, ob ein Benutzer die Shutdown-Methode eines Objekts ausführen kann, die Zeichenfolge "SeShutdownPrivilege" in der **SWbemPrivilege.Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="49901-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the **SWbemPrivilege.Name** property.</span></span> <span data-ttu-id="49901-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="49901-106">This property is read-only.</span></span>

<span data-ttu-id="49901-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="49901-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="49901-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="49901-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49901-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="49901-109">Syntax</span></span>


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a><span data-ttu-id="49901-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="49901-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="49901-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49901-111">Requirements</span></span>



| <span data-ttu-id="49901-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49901-112">Requirement</span></span> | <span data-ttu-id="49901-113">Wert</span><span class="sxs-lookup"><span data-stu-id="49901-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49901-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49901-114">Minimum supported client</span></span><br/> | <span data-ttu-id="49901-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49901-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49901-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49901-116">Minimum supported server</span></span><br/> | <span data-ttu-id="49901-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49901-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49901-118">Header</span><span class="sxs-lookup"><span data-stu-id="49901-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="49901-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="49901-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="49901-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="49901-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="49901-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="49901-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="49901-122">DLL</span><span class="sxs-lookup"><span data-stu-id="49901-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49901-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49901-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="49901-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="49901-124">CLSID</span></span><br/>                    | <span data-ttu-id="49901-125">CLSID- \_ Swap-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="49901-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="49901-126">IID</span><span class="sxs-lookup"><span data-stu-id="49901-126">IID</span></span><br/>                      | <span data-ttu-id="49901-127">IID \_ iswbemprivilege</span><span class="sxs-lookup"><span data-stu-id="49901-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




