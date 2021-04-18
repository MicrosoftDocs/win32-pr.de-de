---
title: IMsRdpClientShell2 securedsettingsenabled (Eigenschaft)
description: Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClientShell2-Schnittstelle
- IMsRdpClientShell2 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340370"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a><span data-ttu-id="07827-106">IMsRdpClientShell2:: securedsettingsenabled (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="07827-106">IMsRdpClientShell2::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="07827-107">Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.</span><span class="sxs-lookup"><span data-stu-id="07827-107">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

<span data-ttu-id="07827-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="07827-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07827-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07827-109">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="07827-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="07827-110">Property value</span></span>

<span data-ttu-id="07827-111">Ein Zeiger auf einen booleschen Wert, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.</span><span class="sxs-lookup"><span data-stu-id="07827-111">A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="07827-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07827-112">Requirements</span></span>



| <span data-ttu-id="07827-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07827-113">Requirement</span></span> | <span data-ttu-id="07827-114">Wert</span><span class="sxs-lookup"><span data-stu-id="07827-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07827-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07827-115">Minimum supported client</span></span><br/> | <span data-ttu-id="07827-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07827-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="07827-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07827-117">Minimum supported server</span></span><br/> | <span data-ttu-id="07827-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07827-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="07827-119">DLL</span><span class="sxs-lookup"><span data-stu-id="07827-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07827-120"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07827-120"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07827-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07827-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07827-122">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="07827-122">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

 





