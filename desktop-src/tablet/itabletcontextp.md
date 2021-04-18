---
description: Stellt den Tablet-Kontext dar.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Itabletcontextp-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351132"
---
# <a name="itabletcontextp-interface"></a><span data-ttu-id="1b3a0-103">Itabletcontextp-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1b3a0-103">ITabletContextP interface</span></span>

<span data-ttu-id="1b3a0-104">Stellt den Tablet-Kontext dar.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-104">Represents the tablet context.</span></span>

## <a name="members"></a><span data-ttu-id="1b3a0-105">Member</span><span class="sxs-lookup"><span data-stu-id="1b3a0-105">Members</span></span>

<span data-ttu-id="1b3a0-106">Die **itabletcontextp** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-106">The **ITabletContextP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1b3a0-107">**Itabletcontextp** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1b3a0-107">**ITabletContextP** also has these types of members:</span></span>

-   [<span data-ttu-id="1b3a0-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1b3a0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1b3a0-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1b3a0-109">Methods</span></span>

<span data-ttu-id="1b3a0-110">Die **itabletcontextp** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-110">The **ITabletContextP** interface has these methods.</span></span>



| <span data-ttu-id="1b3a0-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1b3a0-111">Method</span></span>                                                                                           | <span data-ttu-id="1b3a0-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b3a0-112">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="1b3a0-113">**Istopmosthook**</span><span class="sxs-lookup"><span data-stu-id="1b3a0-113">**IsTopMostHook**</span></span>](itabletcontextp-istopmosthook.md)                                           | <span data-ttu-id="1b3a0-114">Gibt an, ob sich der Tablet-Kontext im Top-Hook befindet.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-114">Indicates if the tablet context is in the top most hook.</span></span><br/>             |
| [<span data-ttu-id="1b3a0-115">**Überlappen**</span><span class="sxs-lookup"><span data-stu-id="1b3a0-115">**Overlap**</span></span>](itabletcontextp-overlap.md)                                                       | <span data-ttu-id="1b3a0-116">Verschiebt einen Tablet-Kontext an die Vorder-oder Rückseite der Eingabe Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-116">Moves a tablet context to the front or back of the input queue.</span></span><br/>      |
| [<span data-ttu-id="1b3a0-117">**Trackinputrect**</span><span class="sxs-lookup"><span data-stu-id="1b3a0-117">**TrackInputRect**</span></span>](itabletcontextp-trackinputrect.md)                                         | <span data-ttu-id="1b3a0-118">Aktualisiert den Tablet-Digitalisierer auf Fenster Speicherort-Mapping-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-118">Updates the tablet digitizer to window location mapping coordinates.</span></span><br/> |
| [<span data-ttu-id="1b3a0-119">**Usenamedsharedmemorycommunications**</span><span class="sxs-lookup"><span data-stu-id="1b3a0-119">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md) | <span data-ttu-id="1b3a0-120">Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben</span><span class="sxs-lookup"><span data-stu-id="1b3a0-120">Provides access to memory shared between tablet threads.</span></span><br/>             |
| [<span data-ttu-id="1b3a0-121">**"US-haredmemorycommunications"**</span><span class="sxs-lookup"><span data-stu-id="1b3a0-121">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)           | <span data-ttu-id="1b3a0-122">Ermöglicht den Zugriff auf Arbeitsspeicher, der für tablettthreads freigegeben</span><span class="sxs-lookup"><span data-stu-id="1b3a0-122">Provides access to memory shared between tablet threads.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="1b3a0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b3a0-123">Remarks</span></span>

<span data-ttu-id="1b3a0-124">Entwickler sollten diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-124">Developers should not use this interface.</span></span>

<span data-ttu-id="1b3a0-125">" [**Usenamedsharedmemorycommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) " ist nur unter Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) is only available on Windows Vista and later.</span></span>

<span data-ttu-id="1b3a0-126">Im folgenden Code wird beschrieben, wie die **itabletcontextp** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1b3a0-126">The following code describes how the **ITabletContextP** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a><span data-ttu-id="1b3a0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b3a0-127">Requirements</span></span>



| <span data-ttu-id="1b3a0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b3a0-128">Requirement</span></span> | <span data-ttu-id="1b3a0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1b3a0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b3a0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b3a0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1b3a0-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b3a0-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1b3a0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b3a0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1b3a0-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1b3a0-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1b3a0-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b3a0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b3a0-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a0-135"><dt>Wisptis.exe</dt></span></span> </dl> |



 

