---
description: Macht diesen Zeiger auf eine Elementbezeichnerliste (PIDL) zu einem ungültigen Teil des Shellordners.
title: IShellFolderSearchable::InvalidateSearch-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841691"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="a1411-103">IShellFolderSearchable::InvalidateSearch-Methode</span><span class="sxs-lookup"><span data-stu-id="a1411-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="a1411-104">Macht diesen Zeiger auf eine Elementbezeichnerliste (PIDL) zu einem ungültigen Teil des Shellordners.</span><span class="sxs-lookup"><span data-stu-id="a1411-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1411-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1411-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a1411-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1411-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1411-107">*pidlSearch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a1411-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1411-108">Typ: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="a1411-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="a1411-109">Ein Zeiger auf die [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für den Suchordner.</span><span class="sxs-lookup"><span data-stu-id="a1411-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="a1411-110">*pdwFlags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a1411-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1411-111">Typ: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="a1411-111">Type: **DWORD\***</span></span>

<span data-ttu-id="a1411-112">Derzeit sind keine Flags definiert. legen Sie auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="a1411-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1411-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1411-113">Return value</span></span>

<span data-ttu-id="a1411-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a1411-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a1411-115">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1411-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1411-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1411-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1411-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1411-117">Remarks</span></span>

<span data-ttu-id="a1411-118">Wenn ein Suchordner für ungültig erklärt wird, kann er eine Bereinigung aller ressourcen durchführen, die er verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="a1411-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="a1411-119">Die **IShellFolderSearchable::InvalidateSearch-Methode** kann dazu führen, dass eine asynchrone Suche abgebrochen wird, was zur endgültigen Veröffentlichung des [**IShellFolderSearchableCallback-Schnittstellenobjekts**](ishellfoldersearchablecallback.md) führt.</span><span class="sxs-lookup"><span data-stu-id="a1411-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1411-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1411-120">Requirements</span></span>



| <span data-ttu-id="a1411-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1411-121">Requirement</span></span> | <span data-ttu-id="a1411-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a1411-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1411-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1411-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a1411-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1411-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a1411-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1411-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a1411-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1411-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a1411-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a1411-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1411-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1411-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




