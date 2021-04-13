---
title: IMsRdpClientNonScriptable5 disableconnectionbar (Eigenschaft)
description: Gibt an, ob das Remotedesktop ActiveX-Steuerelement die Verbindungs Leiste deaktivieren soll.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Disableconnectionbar-Eigenschaft Remotedesktopdienste
- Disableconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, disableconnectionbar (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a129d4781db69a564eecbca3a715c3c5ccf1a9cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519236"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a><span data-ttu-id="81047-106">IMsRdpClientNonScriptable5::D isableconnectionbar-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="81047-106">IMsRdpClientNonScriptable5::DisableConnectionBar property</span></span>

<span data-ttu-id="81047-107">Gibt an, ob das Remotedesktop ActiveX-Steuerelement die Verbindungs Leiste deaktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="81047-107">Specifies whether the Remote Desktop ActiveX control should disable the connection bar.</span></span> <span data-ttu-id="81047-108">Wenn diese Eigenschaft **Variant \_ true** enthält, sollte die Verbindungs Leiste deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="81047-108">If this property contains **VARIANT\_TRUE**, the connection bar should be disabled.</span></span> <span data-ttu-id="81047-109">Wenn diese Eigenschaft **Variant \_ false** enthält, muss die Verbindungs Leiste aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="81047-109">If this property contains **VARIANT\_FALSE**, the connection bar should be enabled.</span></span>

<span data-ttu-id="81047-110">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="81047-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="81047-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="81047-111">Syntax</span></span>


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="81047-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="81047-112">Property value</span></span>

<span data-ttu-id="81047-113">Gibt den neuen Eigenschafts Wert an.</span><span class="sxs-lookup"><span data-stu-id="81047-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="81047-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81047-114">Requirements</span></span>



| <span data-ttu-id="81047-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81047-115">Requirement</span></span> | <span data-ttu-id="81047-116">Wert</span><span class="sxs-lookup"><span data-stu-id="81047-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="81047-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81047-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81047-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81047-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="81047-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81047-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81047-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81047-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="81047-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="81047-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="81047-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81047-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="81047-123">DLL</span><span class="sxs-lookup"><span data-stu-id="81047-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81047-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81047-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="81047-125">IID</span><span class="sxs-lookup"><span data-stu-id="81047-125">IID</span></span><br/>                      | <span data-ttu-id="81047-126">IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.</span><span class="sxs-lookup"><span data-stu-id="81047-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81047-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81047-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81047-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="81047-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





