---
description: Die Manifest-Eigenschaft wird verwendet, um den aktiven Aktivierungs Kontext festzulegen oder zu erhalten.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx. Manifest (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958849"
---
# <a name="actctxmanifest-property"></a><span data-ttu-id="664f9-103">ActCtx. Manifest (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="664f9-103">ActCtx.Manifest property</span></span>

<span data-ttu-id="664f9-104">Die **Manifest** -Eigenschaft wird verwendet, um den aktiven Aktivierungs Kontext festzulegen oder zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="664f9-104">The **Manifest** property is used to set or get the active activation context.</span></span>

<span data-ttu-id="664f9-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="664f9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="664f9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="664f9-106">Syntax</span></span>


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a><span data-ttu-id="664f9-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="664f9-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="664f9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="664f9-108">Remarks</span></span>

<span data-ttu-id="664f9-109">Wenn ein Aktivierungs Kontext mit der angegebenen Manifestressource erstellt werden kann, wird die Manifestressource durch das folgende Skript festgelegt und die durch das Manifest angegebene Aktivierungs Konstante aktiviert.</span><span class="sxs-lookup"><span data-stu-id="664f9-109">If an activation context can be created with the manifest file provided, the following script sets the Manifest property and activates the activation constant specified by the manifest.</span></span> <span data-ttu-id="664f9-110">Wenn kein Aktivierungs Kontext aus dem Manifest erstellt werden kann, bleibt der Aktivierungs Kontext auf den aktuell aktiven Aktivierungs Kontext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="664f9-110">If an activation context cannot be created from the manifest, the activation context remains set to the currently active activation context.</span></span>

<span data-ttu-id="664f9-111">Actctxobj. Manifest = "<*Manifest-Dateiname*>";</span><span class="sxs-lookup"><span data-stu-id="664f9-111">ActCtxObj.Manifest = "<*manifest file name*>";</span></span>

<span data-ttu-id="664f9-112">Wenn zuvor ein Aktivierungs Kontext erstellt oder aktiviert wurde, legt das folgende Skript die **Manifest** -Eigenschaft auf den aktuellen Aktivierungs Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="664f9-112">If an activation context has previously been created or activated, the following script sets the **Manifest** property to the current activation context.</span></span> <span data-ttu-id="664f9-113">Wenn zuvor kein Aktivierungs Kontext erstellt oder aktiviert wurde, wird die Eigenschaft **Manifest** auf eine leere Zeichenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="664f9-113">If an activation context has not previously been created or activated, this sets the **Manifest** property to an empty string.</span></span>

<span data-ttu-id="664f9-114">"BSTR bstrinmanifest = actctxobj. Manifest"</span><span class="sxs-lookup"><span data-stu-id="664f9-114">"BSTR bstrManifest = ActCtxObj.Manifest"</span></span>

## <a name="requirements"></a><span data-ttu-id="664f9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="664f9-115">Requirements</span></span>



| <span data-ttu-id="664f9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="664f9-116">Requirement</span></span> | <span data-ttu-id="664f9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="664f9-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="664f9-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="664f9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="664f9-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="664f9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="664f9-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="664f9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="664f9-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="664f9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="664f9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="664f9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="664f9-123"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="664f9-123"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="664f9-124">IID</span><span class="sxs-lookup"><span data-stu-id="664f9-124">IID</span></span><br/>                      | <span data-ttu-id="664f9-125">IID \_ iactctx ist als 8fa7728f-b69b-4ee5-99f 2-e2aa021bef 28 definiert.</span><span class="sxs-lookup"><span data-stu-id="664f9-125">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



 

 




