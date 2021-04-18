---
description: 'Remotable-Version der imfpmphost:: forateobjectbyclsid-Methode.'
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: Remotekreateobjectbyclsid (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343738"
---
# <a name="remotecreateobjectbyclsid"></a><span data-ttu-id="f0e33-103">Remotekreateobjectbyclsid</span><span class="sxs-lookup"><span data-stu-id="f0e33-103">RemoteCreateObjectByCLSID</span></span>

<span data-ttu-id="f0e33-104">Remotable-Version der [**imfpmphost:: forateobjectbyclsid**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f0e33-104">Remotable version of the [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) method.</span></span>

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a><span data-ttu-id="f0e33-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0e33-105">Remarks</span></span>

<span data-ttu-id="f0e33-106">Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="f0e33-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="f0e33-107">Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0e33-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="f0e33-108">Wenn " [**kreateobjectbyclsid**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) " über Prozess Grenzen hinweg aufgerufen wird, übersetzt die Media Foundation Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt Sie dann zurück.</span><span class="sxs-lookup"><span data-stu-id="f0e33-108">If [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e33-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0e33-109">Requirements</span></span>



| <span data-ttu-id="f0e33-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0e33-110">Requirement</span></span> | <span data-ttu-id="f0e33-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f0e33-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e33-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0e33-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e33-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0e33-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0e33-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0e33-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e33-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0e33-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0e33-116">Header</span><span class="sxs-lookup"><span data-stu-id="f0e33-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0e33-117"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0e33-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="f0e33-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0e33-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0e33-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0e33-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f0e33-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0e33-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e33-121">**Imfpmphost**</span><span class="sxs-lookup"><span data-stu-id="f0e33-121">**IMFPMPHost**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[<span data-ttu-id="f0e33-122">PMP-Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="f0e33-122">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="f0e33-123">Geschützter Medien Pfad</span><span class="sxs-lookup"><span data-stu-id="f0e33-123">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 




