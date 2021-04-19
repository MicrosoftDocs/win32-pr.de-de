---
description: Setzt die Prozesse des Pakets fort, wenn Sie zurzeit angehalten sind.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'Ipackagedebugsettings:: Resume-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344443"
---
# <a name="ipackagedebugsettingsresume-method"></a><span data-ttu-id="27ce4-103">Ipackagedebugsettings:: Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="27ce4-103">IPackageDebugSettings::Resume method</span></span>

<span data-ttu-id="27ce4-104">Setzt die Prozesse des Pakets fort, wenn Sie zurzeit angehalten sind.</span><span class="sxs-lookup"><span data-stu-id="27ce4-104">Resumes the processes of the package if they are currently suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="27ce4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27ce4-105">Syntax</span></span>


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="27ce4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27ce4-107">*packagefullname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27ce4-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27ce4-108">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="27ce4-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="27ce4-109">Der vollständige Paketname.</span><span class="sxs-lookup"><span data-stu-id="27ce4-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27ce4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27ce4-110">Return value</span></span>

<span data-ttu-id="27ce4-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="27ce4-111">Type: **HRESULT**</span></span>

<span data-ttu-id="27ce4-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="27ce4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27ce4-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27ce4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27ce4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27ce4-114">Remarks</span></span>

<span data-ttu-id="27ce4-115">Jeder Prozess empfängt das [**resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="27ce4-115">Each process receives the [**Resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="27ce4-116">Es kann nützlich sein, wenn Entwickler schrittweise durchlaufen, wie Ihre apps auf dieses Ereignis reagieren.</span><span class="sxs-lookup"><span data-stu-id="27ce4-116">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="27ce4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27ce4-117">Requirements</span></span>



| <span data-ttu-id="27ce4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27ce4-118">Requirement</span></span> | <span data-ttu-id="27ce4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="27ce4-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27ce4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27ce4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="27ce4-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="27ce4-121">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="27ce4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27ce4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="27ce4-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27ce4-123">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="27ce4-124">IDL</span><span class="sxs-lookup"><span data-stu-id="27ce4-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27ce4-125"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27ce4-125"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27ce4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27ce4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="27ce4-127">[**Ipackagedebugsettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27ce4-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
