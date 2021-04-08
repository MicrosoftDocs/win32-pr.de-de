---
description: 'Remotable-Version der imfcontentschutzmanager:: dendenablecontent-Methode.'
ms.assetid: aa7a2b3a-5982-4fd8-b5de-7439fc374dfa
title: Remoteendenablecontent (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bab87bc39e930c08b96e1d312932f061f9dd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863415"
---
# <a name="remoteendenablecontent"></a><span data-ttu-id="95f64-103">Remoteendenablecontent</span><span class="sxs-lookup"><span data-stu-id="95f64-103">RemoteEndEnableContent</span></span>

<span data-ttu-id="95f64-104">Remotable-Version der [**imfcontentschutzmanager:: dendenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) -Methode.</span><span class="sxs-lookup"><span data-stu-id="95f64-104">Remotable version of the [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) method.</span></span>

``` syntax
[call_as(EndEnableContent)]
HRESULT RemoteEndEnableContent(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="95f64-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95f64-105">Remarks</span></span>

<span data-ttu-id="95f64-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="95f64-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="95f64-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95f64-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="95f64-108">Wenn " [**erdenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) " über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="95f64-108">If [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f64-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95f64-109">Requirements</span></span>



| <span data-ttu-id="95f64-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95f64-110">Requirement</span></span> | <span data-ttu-id="95f64-111">Wert</span><span class="sxs-lookup"><span data-stu-id="95f64-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f64-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95f64-112">Minimum supported client</span></span><br/> | <span data-ttu-id="95f64-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95f64-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95f64-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95f64-114">Minimum supported server</span></span><br/> | <span data-ttu-id="95f64-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95f64-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95f64-116">Header</span><span class="sxs-lookup"><span data-stu-id="95f64-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="95f64-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95f64-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="95f64-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95f64-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="95f64-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95f64-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="95f64-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95f64-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f64-121">**IMF contentprotection Manager**</span><span class="sxs-lookup"><span data-stu-id="95f64-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




