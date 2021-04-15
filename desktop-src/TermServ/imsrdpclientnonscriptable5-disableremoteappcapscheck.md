---
title: IMsRdpClientNonScriptable5 disableremoteappcapscheck (Eigenschaft)
description: Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Disableremoteappcapscheck-Eigenschaft Remotedesktopdienste
- Disableremoteappcapscheck-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, disableremoteappcapscheck-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479287"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a><span data-ttu-id="9cadb-106">IMsRdpClientNonScriptable5::D isableremoteappcapscheck-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9cadb-106">IMsRdpClientNonScriptable5::DisableRemoteAppCapsCheck property</span></span>

<span data-ttu-id="9cadb-107">Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="9cadb-107">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="9cadb-108">Wenn diese Eigenschaft **Variant \_ true** enthält, sollte das Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9cadb-108">If this property contains **VARIANT\_TRUE**, the control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="9cadb-109">Wenn diese Eigenschaft **Variant \_ false** enthält, kann das Steuerelement den Server auf RemoteApp-Funktionen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9cadb-109">If this property contains **VARIANT\_FALSE**, the control can check the server for RemoteApp capabilities.</span></span>

<span data-ttu-id="9cadb-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9cadb-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cadb-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cadb-111">Syntax</span></span>


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a><span data-ttu-id="9cadb-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9cadb-112">Property value</span></span>

<span data-ttu-id="9cadb-113">Gibt den neuen Eigenschafts Wert an.</span><span class="sxs-lookup"><span data-stu-id="9cadb-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cadb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cadb-114">Requirements</span></span>



| <span data-ttu-id="9cadb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cadb-115">Requirement</span></span> | <span data-ttu-id="9cadb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9cadb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cadb-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9cadb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9cadb-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cadb-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9cadb-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9cadb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9cadb-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9cadb-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="9cadb-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9cadb-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="9cadb-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cadb-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9cadb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9cadb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cadb-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cadb-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9cadb-125">IID</span><span class="sxs-lookup"><span data-stu-id="9cadb-125">IID</span></span><br/>                      | <span data-ttu-id="9cadb-126">IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.</span><span class="sxs-lookup"><span data-stu-id="9cadb-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9cadb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cadb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cadb-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="9cadb-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





