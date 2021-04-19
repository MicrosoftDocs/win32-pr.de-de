---
description: 'Remotable-Version der imfcontentschutzmanager:: beginenablecontent-Methode.'
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: Remotebeginenablecontent (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9bc4a445ec07a7e9678a9d0a193311554f855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345197"
---
# <a name="remotebeginenablecontent"></a><span data-ttu-id="dfa42-103">Remotebeginenablecontent</span><span class="sxs-lookup"><span data-stu-id="dfa42-103">RemoteBeginEnableContent</span></span>

<span data-ttu-id="dfa42-104">Remotable-Version der [**imfcontentschutzmanager:: beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dfa42-104">Remotable version of the [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="dfa42-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfa42-105">Remarks</span></span>

<span data-ttu-id="dfa42-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="dfa42-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="dfa42-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dfa42-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="dfa42-108">Wenn [**beginenablecontent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="dfa42-108">If [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa42-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfa42-109">Requirements</span></span>



| <span data-ttu-id="dfa42-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfa42-110">Requirement</span></span> | <span data-ttu-id="dfa42-111">Wert</span><span class="sxs-lookup"><span data-stu-id="dfa42-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa42-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfa42-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa42-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfa42-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dfa42-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfa42-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa42-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfa42-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dfa42-116">Header</span><span class="sxs-lookup"><span data-stu-id="dfa42-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfa42-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfa42-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="dfa42-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dfa42-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfa42-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfa42-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="dfa42-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfa42-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa42-121">**IMF contentprotection Manager**</span><span class="sxs-lookup"><span data-stu-id="dfa42-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




