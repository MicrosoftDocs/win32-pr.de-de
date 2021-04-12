---
title: Imsrdpclientadvancedsettings (sassequence-Eigenschaft)
description: Gibt die Secure Access Sequence (SAS) an, mit der der Client auf den Anmeldebildschirm auf dem Server zugreift.
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- Sassequence-Eigenschaft Remotedesktopdienste
- Sassequence-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, sassequence-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475234"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a><span data-ttu-id="76e67-106">Imsrdpclientadvancedsettings:: sassequence (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="76e67-106">IMsRdpClientAdvancedSettings::SasSequence property</span></span>

<span data-ttu-id="76e67-107">Gibt die Secure Access Sequence (SAS) an, mit der der Client auf den Anmeldebildschirm auf dem Server zugreift.</span><span class="sxs-lookup"><span data-stu-id="76e67-107">Specifies the secure access sequence (SAS) the client will use to access the login screen on the server.</span></span>

<span data-ttu-id="76e67-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="76e67-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="76e67-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76e67-109">Syntax</span></span>


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a><span data-ttu-id="76e67-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="76e67-110">Property value</span></span>

<span data-ttu-id="76e67-111">Ein **Long** -Wert, der den SAS-Indikator enthält.</span><span class="sxs-lookup"><span data-stu-id="76e67-111">A **LONG** value that contains the SAS indicator.</span></span> <span data-ttu-id="76e67-112">Der einzige unterstützte Wert ist 0xaa03, der die Standard Sequenz STRG + ALT + ENTF angibt.</span><span class="sxs-lookup"><span data-stu-id="76e67-112">The only supported value is 0xaa03, which indicates the standard CTRL+ALT+DELETE sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="76e67-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76e67-113">Remarks</span></span>

<span data-ttu-id="76e67-114">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="76e67-114">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76e67-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76e67-115">Requirements</span></span>



| <span data-ttu-id="76e67-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76e67-116">Requirement</span></span> | <span data-ttu-id="76e67-117">Wert</span><span class="sxs-lookup"><span data-stu-id="76e67-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76e67-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76e67-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76e67-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76e67-119">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="76e67-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76e67-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76e67-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76e67-121">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="76e67-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="76e67-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="76e67-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76e67-123"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="76e67-124">DLL</span><span class="sxs-lookup"><span data-stu-id="76e67-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76e67-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76e67-125"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="76e67-126">IID</span><span class="sxs-lookup"><span data-stu-id="76e67-126">IID</span></span><br/>                      | <span data-ttu-id="76e67-127">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="76e67-127">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76e67-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76e67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76e67-129">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="76e67-129">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





