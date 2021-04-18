---
description: Ruft den imsdxgidebug Manager aus der Microsoft Media Foundation Video Rendering-Senke ab.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'IMF dxgidevicemanagersource:: GetManager-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343842"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a><span data-ttu-id="30a9f-103">IMF dxgidevicemanagersource:: GetManager-Methode</span><span class="sxs-lookup"><span data-stu-id="30a9f-103">IMFDXGIDeviceManagerSource::GetManager method</span></span>

<span data-ttu-id="30a9f-104">Ruft den [**imsdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) aus der Microsoft Media Foundation Video Rendering-Senke ab.</span><span class="sxs-lookup"><span data-stu-id="30a9f-104">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a9f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a9f-105">Syntax</span></span>


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="30a9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30a9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a9f-107">*ppManager* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="30a9f-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a9f-108">Das [**IMF dxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="30a9f-108">The [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a9f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30a9f-109">Return value</span></span>

<span data-ttu-id="30a9f-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="30a9f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30a9f-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30a9f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a9f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30a9f-112">Requirements</span></span>



| <span data-ttu-id="30a9f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30a9f-113">Requirement</span></span> | <span data-ttu-id="30a9f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="30a9f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30a9f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30a9f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="30a9f-116">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="30a9f-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="30a9f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30a9f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="30a9f-118">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="30a9f-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="30a9f-119">IDL</span><span class="sxs-lookup"><span data-stu-id="30a9f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30a9f-120"><dt>MFI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30a9f-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a9f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a9f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a9f-122">**IMF-xgide vicemanagersource**</span><span class="sxs-lookup"><span data-stu-id="30a9f-122">**IMFDXGIDeviceManagerSource**</span></span>](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




