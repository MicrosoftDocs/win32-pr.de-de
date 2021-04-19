---
description: Legt die Liste der beibehaltenen Gruppen-IDs für alle Profile fest, die von Ihrer APP persistent gespeichert werden.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Wfddisplaysink setpersistedgroupidlist-Funktion (wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347047"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a><span data-ttu-id="7cb51-103">Wfddisplaysink setpersistedgroupidlist-Funktion</span><span class="sxs-lookup"><span data-stu-id="7cb51-103">WFDDisplaySinkSetPersistedGroupIDList function</span></span>

<span data-ttu-id="7cb51-104">Legt die Liste der beibehaltenen Gruppen-IDs für alle Profile fest, die von Ihrer APP persistent gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7cb51-104">Sets the persisted group id list for all the profiles that are persisted by your app.</span></span> <span data-ttu-id="7cb51-105">Ihre APP sollte diese Methode jedes Mal aufgerufen werden, wenn Sie ein Profil aus dem Speicher hinzufügt oder löscht.</span><span class="sxs-lookup"><span data-stu-id="7cb51-105">Your app should call this method every time it adds or deletes a profile from its storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb51-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cb51-106">Syntax</span></span>


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a><span data-ttu-id="7cb51-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cb51-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cb51-108">*cgroupidlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cb51-108">*cGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb51-109">Die Anzahl der Gruppen-IDs, auf die von *pgroupidlist* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7cb51-109">The count of group ids being pointed to by *pGroupIDList*.</span></span>

</dd> <dt>

<span data-ttu-id="7cb51-110">*pgroupidlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cb51-110">*pGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb51-111">Zeiger auf ein Array aus *cgroupidlist* -Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="7cb51-111">Pointer to an array of *cGroupIDList* group ids.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cb51-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cb51-112">Return value</span></span>

<span data-ttu-id="7cb51-113">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7cb51-113">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb51-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cb51-114">Remarks</span></span>

<span data-ttu-id="7cb51-115">Es wird immer erwartet, dass diese Methode mit der gesamten Liste und nicht mit einer Teilmenge aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7cb51-115">This method is always expected to be called with the entire list, and not a subset.</span></span> <span data-ttu-id="7cb51-116">Es ist in Ordnung, diese Methode mit 0 Profilen aufzurufen, wenn der Profil Speicher leer ist.</span><span class="sxs-lookup"><span data-stu-id="7cb51-116">It is OK to call this method with 0 profiles when the profile store is empty.</span></span>

<span data-ttu-id="7cb51-117">Ein erneutes aufrufen für eine Gruppen-ID, die nicht Teil der angegebenen Liste ist, schlägt fehl mit "Fail; Unbekannte P2P-Gruppe "(Status 8).</span><span class="sxs-lookup"><span data-stu-id="7cb51-117">A re-invoke for a group id that is not part of the provided list will fail with "Fail; unknown P2P Group"(status 8).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb51-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cb51-118">Requirements</span></span>



| <span data-ttu-id="7cb51-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cb51-119">Requirement</span></span> | <span data-ttu-id="7cb51-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7cb51-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb51-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cb51-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb51-122">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="7cb51-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7cb51-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cb51-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb51-124">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cb51-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cb51-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7cb51-125">End of client support</span></span><br/>    | <span data-ttu-id="7cb51-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7cb51-126">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="7cb51-127">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7cb51-127">End of server support</span></span><br/>    | <span data-ttu-id="7cb51-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7cb51-128">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="7cb51-129">Header</span><span class="sxs-lookup"><span data-stu-id="7cb51-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cb51-130"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cb51-130"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="7cb51-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7cb51-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cb51-132"><dt>Wifdisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cb51-132"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="7cb51-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7cb51-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cb51-134"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cb51-134"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




