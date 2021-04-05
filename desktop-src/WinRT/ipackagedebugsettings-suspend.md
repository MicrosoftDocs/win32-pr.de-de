---
description: Hält die Prozesse des Pakets an, wenn Sie derzeit ausgeführt werden.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Ipackagedebugsettings:: Suspend-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751496"
---
# <a name="ipackagedebugsettingssuspend-method"></a><span data-ttu-id="11ef7-103">Ipackagedebugsettings:: Suspend-Methode</span><span class="sxs-lookup"><span data-stu-id="11ef7-103">IPackageDebugSettings::Suspend method</span></span>

<span data-ttu-id="11ef7-104">Hält die Prozesse des Pakets an, wenn Sie derzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="11ef7-104">Suspends the processes of the package if they are currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ef7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11ef7-105">Syntax</span></span>


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="11ef7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11ef7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ef7-107">*packagefullname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11ef7-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11ef7-108">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="11ef7-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="11ef7-109">Der vollständige Paketname.</span><span class="sxs-lookup"><span data-stu-id="11ef7-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ef7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11ef7-110">Return value</span></span>

<span data-ttu-id="11ef7-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="11ef7-111">Type: **HRESULT**</span></span>

<span data-ttu-id="11ef7-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="11ef7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="11ef7-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="11ef7-113">Return code</span></span>                                                                                            | <span data-ttu-id="11ef7-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11ef7-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="11ef7-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11ef7-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="11ef7-116">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11ef7-116">The operation succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="11ef7-117"><dt>**E ungültige \_ \_ StateChange**</dt></span><span class="sxs-lookup"><span data-stu-id="11ef7-117"><dt>**E\_ILLEGAL\_STATECHANGE**</dt></span></span> </dl> | <span data-ttu-id="11ef7-118">Der Prozess wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11ef7-118">The process is not currently running.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11ef7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11ef7-119">Remarks</span></span>

<span data-ttu-id="11ef7-120">Jeder Prozess empfängt das [**Suspensions**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) Ereignis.</span><span class="sxs-lookup"><span data-stu-id="11ef7-120">Each process receives the [**Suspending**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="11ef7-121">Es kann nützlich sein, wenn Entwickler schrittweise durchlaufen, wie Ihre apps auf dieses Ereignis reagieren.</span><span class="sxs-lookup"><span data-stu-id="11ef7-121">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ef7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11ef7-122">Requirements</span></span>



| <span data-ttu-id="11ef7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11ef7-123">Requirement</span></span> | <span data-ttu-id="11ef7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="11ef7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11ef7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11ef7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11ef7-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="11ef7-126">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="11ef7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11ef7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11ef7-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11ef7-128">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="11ef7-129">IDL</span><span class="sxs-lookup"><span data-stu-id="11ef7-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11ef7-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11ef7-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ef7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11ef7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="11ef7-132">[**Ipackagedebugsettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11ef7-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
