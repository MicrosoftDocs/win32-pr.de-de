---
description: Ruft die Standard Kontingent Grenze als Text Zeichenfolge ab.
title: Diskquotacontrol. defaultquotalimittext-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 442e9094c62f22c3d990cf1112d145a1b2838e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128441"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="e8a77-103">Diskquotacontrol. defaultquotalimittext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8a77-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="e8a77-104">Ruft die Standard Kontingent Grenze als Text Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="e8a77-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="e8a77-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e8a77-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a77-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8a77-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="e8a77-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e8a77-107">Property value</span></span>

<span data-ttu-id="e8a77-108">Ein Zeichen folgen Wert, der die Standard Kontingent Grenze für neue Benutzer des Volumes enthält.</span><span class="sxs-lookup"><span data-stu-id="e8a77-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="e8a77-109">Wenn das Standard Kontingent beispielsweise 10,5 MB beträgt, lautet der Wert der Eigenschaft "10,5 MB".</span><span class="sxs-lookup"><span data-stu-id="e8a77-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="e8a77-110">Wenn für das Volume kein Standard Kontingent festgelegt ist, wird die-Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8a77-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a77-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e8a77-111">Requirements</span></span>



| <span data-ttu-id="e8a77-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8a77-112">Requirement</span></span> | <span data-ttu-id="e8a77-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e8a77-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a77-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8a77-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a77-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8a77-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8a77-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8a77-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a77-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8a77-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e8a77-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e8a77-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8a77-119"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="e8a77-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a77-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8a77-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a77-121">**Defaultquotalimit**</span><span class="sxs-lookup"><span data-stu-id="e8a77-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="e8a77-122">**Diskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="e8a77-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




