---
title: IMsRdpClientNonScriptable5 remotemonitorlayoutmatcheslocal (Eigenschaft)
description: Gibt an, ob das Remote Monitor Layout mit dem Layout des lokalen Monitors identisch ist.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Remotemonitorlayoutmatcheslocal-Eigenschaft Remotedesktopdienste
- Remotemonitorlayoutmatcheslocal-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, remotemonitorlayoutmatcheslocal (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104619"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a><span data-ttu-id="e8a5e-106">IMsRdpClientNonScriptable5:: remotemonitorlayoutmatcheslocal (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e8a5e-106">IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal property</span></span>

<span data-ttu-id="e8a5e-107">Gibt an, ob das Remote Monitor Layout mit dem Layout des lokalen Monitors identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-107">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="e8a5e-108">Wenn diese Eigenschaft **Variant \_ true** enthält, ist das Layout des Remote Monitors mit dem Layout des lokalen Monitors identisch.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-108">If this property contains **VARIANT\_TRUE**, the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="e8a5e-109">Wenn diese Eigenschaft **Variant \_ false** enthält, haben die Remote-und lokalen Monitore unterschiedliche Layouts.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-109">If this property contains **VARIANT\_FALSE**, the remote and local monitors have different layouts.</span></span>

<span data-ttu-id="e8a5e-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a5e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8a5e-111">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a><span data-ttu-id="e8a5e-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e8a5e-112">Property value</span></span>

<span data-ttu-id="e8a5e-113">Empfängt den-Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-113">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a5e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8a5e-114">Requirements</span></span>



| <span data-ttu-id="e8a5e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8a5e-115">Requirement</span></span> | <span data-ttu-id="e8a5e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e8a5e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a5e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8a5e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a5e-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8a5e-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8a5e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8a5e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a5e-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8a5e-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="e8a5e-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e8a5e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8a5e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8a5e-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e8a5e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e8a5e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8a5e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8a5e-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e8a5e-125">IID</span><span class="sxs-lookup"><span data-stu-id="e8a5e-125">IID</span></span><br/>                      | <span data-ttu-id="e8a5e-126">IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8a5e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8a5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a5e-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e8a5e-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





