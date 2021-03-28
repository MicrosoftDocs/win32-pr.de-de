---
description: Startet das Abbrechen einer ausstehenden asynchronen Suche.
title: 'Ishellfoldersearchable:: cancelasyncsearch-Methode'
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
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977953"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="0b719-103">Ishellfoldersearchable:: cancelasyncsearch-Methode</span><span class="sxs-lookup"><span data-stu-id="0b719-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="0b719-104">Startet das Abbrechen einer ausstehenden asynchronen Suche.</span><span class="sxs-lookup"><span data-stu-id="0b719-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b719-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b719-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0b719-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b719-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b719-107">*pidlsearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b719-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b719-108">Typ: **lpcitemittellist**</span><span class="sxs-lookup"><span data-stu-id="0b719-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="0b719-109">Ein Zeiger auf eine [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für die Suche.</span><span class="sxs-lookup"><span data-stu-id="0b719-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="0b719-110">*pdwflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b719-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b719-111">Typ: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="0b719-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="0b719-112">Zurzeit sind keine Flags definiert. Legen Sie auf _ \* NULL \* \* fest.</span><span class="sxs-lookup"><span data-stu-id="0b719-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b719-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b719-113">Return value</span></span>

<span data-ttu-id="0b719-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0b719-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0b719-115">Gibt s \_ OK zurück, wenn abgebrochen wird, oder s \_ false, wenn die Suche nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b719-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b719-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b719-116">Remarks</span></span>

<span data-ttu-id="0b719-117">Wenn die Suche tatsächlich abgebrochen wird, wird [**RunEnd**](ishellfoldersearchablecallback-runend.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0b719-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b719-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0b719-118">Requirements</span></span>



| <span data-ttu-id="0b719-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b719-119">Requirement</span></span> | <span data-ttu-id="0b719-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0b719-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b719-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b719-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b719-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b719-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0b719-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b719-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b719-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b719-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b719-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0b719-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b719-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b719-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




