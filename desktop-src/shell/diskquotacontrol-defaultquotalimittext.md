---
description: Ruft die Standardkontingentgrenze als Textzeichenfolge ab.
title: DiskQuotaControl.DefaultQuotaLimitText -Eigenschaft
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
ms.openlocfilehash: 14a5b5a0cc42bda17f922020a8485430797875e1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841541"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="fd9d8-103">DiskQuotaControl.DefaultQuotaLimitText -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd9d8-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="fd9d8-104">Ruft die Standardkontingentgrenze als Textzeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="fd9d8-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="fd9d8-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fd9d8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9d8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd9d8-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="fd9d8-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fd9d8-107">Property value</span></span>

<span data-ttu-id="fd9d8-108">Ein Zeichenfolgenwert, der die Standardkontingentgrenze für neue Benutzer des Volumes enthält.</span><span class="sxs-lookup"><span data-stu-id="fd9d8-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="fd9d8-109">Wenn das Standardkontingent beispielsweise 10,5 MB beträgt, ist der Wert der -Eigenschaft "10,5 MB".</span><span class="sxs-lookup"><span data-stu-id="fd9d8-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="fd9d8-110">Wenn das Volume über kein Standardkontingent verfügt, wird die -Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd9d8-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9d8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd9d8-111">Requirements</span></span>



| <span data-ttu-id="fd9d8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd9d8-112">Requirement</span></span> | <span data-ttu-id="fd9d8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fd9d8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9d8-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd9d8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9d8-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd9d8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd9d8-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd9d8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9d8-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd9d8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd9d8-118">DLL</span><span class="sxs-lookup"><span data-stu-id="fd9d8-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd9d8-119"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fd9d8-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd9d8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd9d8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9d8-121">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="fd9d8-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="fd9d8-122">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="fd9d8-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




