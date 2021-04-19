---
description: 'Remote fähige Version der imfsourceresolver:: beginkreateobjectfrombytestream-Methode.'
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: Remotebeginkreateobjectfromb testream (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348239"
---
# <a name="remotebegincreateobjectfrombytestream"></a><span data-ttu-id="f495b-103">Remotebeginkreateobjectfromb testream</span><span class="sxs-lookup"><span data-stu-id="f495b-103">RemoteBeginCreateObjectFromByteStream</span></span>

<span data-ttu-id="f495b-104">Remote fähige Version der [**imfsourceresolver:: beginkreateobjectfrombytestream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f495b-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="f495b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f495b-105">Remarks</span></span>

<span data-ttu-id="f495b-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="f495b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="f495b-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f495b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="f495b-108">Wenn [**beginkreateobjectfromb-testream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.</span><span class="sxs-lookup"><span data-stu-id="f495b-108">If [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="f495b-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f495b-109">Requirements</span></span>



| <span data-ttu-id="f495b-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f495b-110">Requirement</span></span> | <span data-ttu-id="f495b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f495b-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f495b-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f495b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f495b-113">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f495b-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="f495b-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f495b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f495b-115">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f495b-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="f495b-116">Header</span><span class="sxs-lookup"><span data-stu-id="f495b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f495b-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f495b-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="f495b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f495b-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="f495b-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f495b-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f495b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f495b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f495b-121">**IMF sourceresolver**</span><span class="sxs-lookup"><span data-stu-id="f495b-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




