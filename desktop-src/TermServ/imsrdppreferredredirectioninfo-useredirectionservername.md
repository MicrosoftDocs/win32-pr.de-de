---
title: Imsrdppreferredredirectioninfo useredirectionservername-Eigenschaft
description: Ruft ab und legt fest, ob der Umleitungs Servername verwendet werden soll.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Useredirectionservername-Eigenschaft Remotedesktopdienste
- Useredirectionservername-Eigenschaft Remotedesktopdienste, imsrdppreferredredirectioninfo-Schnittstelle
- Imsrdppreferredredirectioninfo-Schnittstelle Remotedesktopdienste, useredirectionservername-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740760"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a><span data-ttu-id="8d946-106">Imsrdppreferredredirectioninfo:: useredirectionservername-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d946-106">IMsRdpPreferredRedirectionInfo::UseRedirectionServerName property</span></span>

<span data-ttu-id="8d946-107">Ruft ab und legt fest, ob der Umleitungs Servername verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d946-107">Gets and sets whether to use the redirection server name.</span></span>

<span data-ttu-id="8d946-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8d946-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d946-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d946-109">Syntax</span></span>


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a><span data-ttu-id="8d946-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8d946-110">Property value</span></span>

<span data-ttu-id="8d946-111">Gibt an, ob der Umleitungs Servername verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d946-111">Whether to use the redirection server name.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d946-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d946-112">Requirements</span></span>



| <span data-ttu-id="8d946-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d946-113">Requirement</span></span> | <span data-ttu-id="8d946-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8d946-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d946-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d946-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8d946-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8d946-116">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="8d946-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d946-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8d946-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d946-118">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="8d946-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8d946-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d946-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d946-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8d946-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8d946-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d946-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d946-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8d946-123">IID</span><span class="sxs-lookup"><span data-stu-id="8d946-123">IID</span></span><br/>                      | <span data-ttu-id="8d946-124">IID \_ imsrdppreferredredirectioninfo ist als FDD029F9-9574-4DEF-8529-64B521CCCAA4 definiert.</span><span class="sxs-lookup"><span data-stu-id="8d946-124">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d946-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d946-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d946-126">**Imsrdppreferredredirectioninfo**</span><span class="sxs-lookup"><span data-stu-id="8d946-126">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





