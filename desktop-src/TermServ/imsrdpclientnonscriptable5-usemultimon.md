---
title: IMsRdpClientNonScriptable5 usemultimon (Eigenschaft)
description: Gibt an, ob das Remotedesktop ActiveX-Steuerelement mehrere Monitore verwenden soll.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- Usemultimon-Eigenschaft Remotedesktopdienste
- Usemultimon-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste, usemultimon-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956756"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a><span data-ttu-id="ad691-106">IMsRdpClientNonScriptable5:: usemultimon-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad691-106">IMsRdpClientNonScriptable5::UseMultimon property</span></span>

<span data-ttu-id="ad691-107">Gibt an, ob das Remotedesktop ActiveX-Steuerelement mehrere Monitore verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="ad691-107">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span> <span data-ttu-id="ad691-108">Wenn diese Eigenschaft **Variant \_ true** enthält, werden vom Steuerelement mehrere Monitore verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad691-108">If this property contains **VARIANT\_TRUE**, the control will use multiple monitors.</span></span> <span data-ttu-id="ad691-109">Wenn diese Eigenschaft **Variant \_ false** enthält, werden vom Steuerelement nicht mehrere Monitore verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad691-109">If this property contains **VARIANT\_FALSE**, the control will not use multiple monitors.</span></span>

<span data-ttu-id="ad691-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ad691-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad691-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad691-111">Syntax</span></span>


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a><span data-ttu-id="ad691-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ad691-112">Property value</span></span>

<span data-ttu-id="ad691-113">Gibt den neuen Eigenschafts Wert an.</span><span class="sxs-lookup"><span data-stu-id="ad691-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad691-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad691-114">Requirements</span></span>



| <span data-ttu-id="ad691-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad691-115">Requirement</span></span> | <span data-ttu-id="ad691-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ad691-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad691-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad691-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad691-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad691-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ad691-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad691-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad691-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad691-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="ad691-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ad691-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad691-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad691-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ad691-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ad691-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad691-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad691-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ad691-125">IID</span><span class="sxs-lookup"><span data-stu-id="ad691-125">IID</span></span><br/>                      | <span data-ttu-id="ad691-126">IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.</span><span class="sxs-lookup"><span data-stu-id="ad691-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad691-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad691-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad691-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ad691-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





