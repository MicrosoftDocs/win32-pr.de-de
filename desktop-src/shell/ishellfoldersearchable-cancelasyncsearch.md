---
description: Startet den Prozess des Abbrechens einer ausstehenden asynchronen Suche.
title: IShellFolderSearchable::CancelAsyncSearch-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842991"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="71c66-103">IShellFolderSearchable::CancelAsyncSearch-Methode</span><span class="sxs-lookup"><span data-stu-id="71c66-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="71c66-104">Startet den Prozess des Abbrechens einer ausstehenden asynchronen Suche.</span><span class="sxs-lookup"><span data-stu-id="71c66-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71c66-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="71c66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71c66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c66-107">*pidlSearch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="71c66-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c66-108">Typ: **LPJSMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="71c66-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="71c66-109">Ein Zeiger auf eine [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für die Suche.</span><span class="sxs-lookup"><span data-stu-id="71c66-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="71c66-110">*pdwFlags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="71c66-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c66-111">Typ: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="71c66-111">Type: **DWORD\***</span></span>

<span data-ttu-id="71c66-112">Derzeit sind keine Flags definiert. auf **NULL festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="71c66-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c66-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71c66-113">Return value</span></span>

<span data-ttu-id="71c66-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71c66-114">Type: **HRESULT**</span></span>

<span data-ttu-id="71c66-115">Gibt S \_ OK zurück, wenn der Vorgang abgebrochen wird, oder S \_ FALSE, wenn die Suche nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71c66-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="71c66-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="71c66-116">Remarks</span></span>

<span data-ttu-id="71c66-117">Wenn die Suche tatsächlich abgebrochen wird, [**wird RunEnd**](ishellfoldersearchablecallback-runend.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="71c66-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="71c66-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71c66-118">Requirements</span></span>



| <span data-ttu-id="71c66-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71c66-119">Requirement</span></span> | <span data-ttu-id="71c66-120">Wert</span><span class="sxs-lookup"><span data-stu-id="71c66-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71c66-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71c66-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71c66-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71c66-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71c66-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71c66-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71c66-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71c66-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="71c66-125">DLL</span><span class="sxs-lookup"><span data-stu-id="71c66-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71c66-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71c66-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




