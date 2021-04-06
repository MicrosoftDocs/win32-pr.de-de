---
title: IMsRdpClientAdvancedSettings7 enablesuperpan (Eigenschaft)
description: Gibt einen booleschen Wert an, der angibt, ob superpan aktiviert oder deaktiviert ist, oder ruft diesen ab.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Enablesuperpan-Eigenschaft Remotedesktopdienste
- Enablesuperpan-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, enablesuperpan (Eigenschaft)
- Enablesuperpan-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, enablesuperpan (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742136"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a><span data-ttu-id="05476-108">IMsRdpClientAdvancedSettings7:: enablesuperpan (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05476-108">IMsRdpClientAdvancedSettings7::EnableSuperPan property</span></span>

<span data-ttu-id="05476-109">Gibt einen booleschen Wert an, der angibt, ob superpan aktiviert oder deaktiviert ist, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="05476-109">Specifies or retrieves a Boolean value that indicates whether SuperPan is enabled or disabled.</span></span> <span data-ttu-id="05476-110">Superpan ist ein Feature, mit dem Benutzer problemlos im Vollbildmodus auf einem Remote Desktop navigieren können, wenn die Dimensionen des Remote Desktops größer sind als die Dimensionen des aktuellen Client Fensters.</span><span class="sxs-lookup"><span data-stu-id="05476-110">SuperPan is a feature that allows a user to easily navigate a remote desktop in full-screen mode, when the dimensions of the remote desktop are larger than the dimensions of the current client window.</span></span> <span data-ttu-id="05476-111">Anstatt Scrollleisten zum Navigieren im Desktop zu verwenden, kann der Benutzer auf den Fensterrahmen zeigen, und der Remote Desktop führt in dieser Richtung automatisch einen Bildlauf durch.</span><span class="sxs-lookup"><span data-stu-id="05476-111">Instead of using scroll bars to navigate the desktop, the user can point to the window border, and the remote desktop will scroll automatically in that direction.</span></span> <span data-ttu-id="05476-112">Superpan unterstützt nicht mehr als einen Monitor.</span><span class="sxs-lookup"><span data-stu-id="05476-112">SuperPan does not support more than one monitor.</span></span>

<span data-ttu-id="05476-113">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="05476-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="05476-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="05476-114">Syntax</span></span>


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a><span data-ttu-id="05476-115">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="05476-115">Property value</span></span>

<span data-ttu-id="05476-116">Ein **Variant- \_ boolescher** Wert, der angibt, ob superpan aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05476-116">A **VARIANT\_BOOL** value that specifies whether SuperPan is enabled.</span></span> <span data-ttu-id="05476-117">Der Wert **Variant \_ true** gibt an, dass superpan aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05476-117">A value of **VARIANT\_TRUE** specifies that SuperPan is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="05476-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05476-118">Requirements</span></span>



| <span data-ttu-id="05476-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05476-119">Requirement</span></span> | <span data-ttu-id="05476-120">Wert</span><span class="sxs-lookup"><span data-stu-id="05476-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05476-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05476-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05476-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05476-122">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="05476-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05476-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05476-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="05476-124">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="05476-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="05476-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="05476-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05476-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="05476-127">DLL</span><span class="sxs-lookup"><span data-stu-id="05476-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05476-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05476-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="05476-129">IID</span><span class="sxs-lookup"><span data-stu-id="05476-129">IID</span></span><br/>                      | <span data-ttu-id="05476-130">IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.</span><span class="sxs-lookup"><span data-stu-id="05476-130">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05476-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05476-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05476-132">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="05476-132">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="05476-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="05476-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





