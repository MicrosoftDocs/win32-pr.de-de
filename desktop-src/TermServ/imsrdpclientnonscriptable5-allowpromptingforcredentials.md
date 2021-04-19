---
title: IMsRdpClientNonScriptable5 allowpromptingforanmeldeinformationen (Eigenschaft)
description: Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmelde Informationen auffordert.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Allowpromptingforanmelde-Eigenschaft Remotedesktopdienste
- Allowpromptingforanmelde-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, allowpromptingforanmeldeinformationen (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345341"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a><span data-ttu-id="2d689-106">IMsRdpClientNonScriptable5:: allowpromptingforanmeldeinformationen (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2d689-106">IMsRdpClientNonScriptable5::AllowPromptingForCredentials property</span></span>

<span data-ttu-id="2d689-107">Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmelde Informationen auffordert.</span><span class="sxs-lookup"><span data-stu-id="2d689-107">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span> <span data-ttu-id="2d689-108">Wenn diese Eigenschaft **Variant \_ true** enthält, kann der Benutzer zur Eingabe von Anmelde Informationen aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2d689-108">If this property contains **VARIANT\_TRUE**, the user can be prompted for credentials.</span></span> <span data-ttu-id="2d689-109">Wenn diese Eigenschaft **Variant \_ false** enthält, kann der Benutzer nicht zur Eingabe von Anmelde Informationen aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2d689-109">If this property contains **VARIANT\_FALSE**, the user cannot be prompted for credentials.</span></span>

<span data-ttu-id="2d689-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2d689-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d689-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d689-111">Syntax</span></span>


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a><span data-ttu-id="2d689-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2d689-112">Property value</span></span>

<span data-ttu-id="2d689-113">Gibt den neuen Eigenschafts Wert an.</span><span class="sxs-lookup"><span data-stu-id="2d689-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d689-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d689-114">Requirements</span></span>



| <span data-ttu-id="2d689-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d689-115">Requirement</span></span> | <span data-ttu-id="2d689-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2d689-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d689-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d689-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d689-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d689-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d689-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d689-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d689-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d689-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="2d689-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2d689-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d689-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d689-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2d689-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2d689-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d689-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d689-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2d689-125">IID</span><span class="sxs-lookup"><span data-stu-id="2d689-125">IID</span></span><br/>                      | <span data-ttu-id="2d689-126">IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.</span><span class="sxs-lookup"><span data-stu-id="2d689-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d689-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d689-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d689-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2d689-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





