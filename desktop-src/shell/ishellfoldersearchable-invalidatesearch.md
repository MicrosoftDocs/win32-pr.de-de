---
description: Legt diesen Zeiger auf eine Element Bezeichner-Liste (PIDL) als ungültigen Teil des shellordners.
title: 'Ishellfoldersearchable:: invalidatesearch-Methode'
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
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214870"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="ac9b3-103">Ishellfoldersearchable:: invalidatesearch-Methode</span><span class="sxs-lookup"><span data-stu-id="ac9b3-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="ac9b3-104">Legt diesen Zeiger auf eine Element Bezeichner-Liste (PIDL) als ungültigen Teil des shellordners.</span><span class="sxs-lookup"><span data-stu-id="ac9b3-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac9b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac9b3-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ac9b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac9b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac9b3-107">*pidlsearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac9b3-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac9b3-108">Typ: **lpcitemittellist**</span><span class="sxs-lookup"><span data-stu-id="ac9b3-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="ac9b3-109">Ein Zeiger auf die [**itemittellist**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur für den Suchordner.</span><span class="sxs-lookup"><span data-stu-id="ac9b3-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="ac9b3-110">*pdwflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac9b3-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac9b3-111">Typ: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="ac9b3-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="ac9b3-112">Zurzeit sind keine Flags definiert. Legen Sie auf _ \* NULL \* \* fest.</span><span class="sxs-lookup"><span data-stu-id="ac9b3-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac9b3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac9b3-113">Return value</span></span>

<span data-ttu-id="ac9b3-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac9b3-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ac9b3-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ac9b3-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac9b3-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ac9b3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac9b3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac9b3-117">Remarks</span></span>

<span data-ttu-id="ac9b3-118">Wenn ein Suchordner ungültig wird, kann er die Bereinigung aller verwendeten Ressourcen ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac9b3-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="ac9b3-119">Die **ishellfoldersearchable:: invalidatesearch** -Methode kann bewirken, dass eine asynchrone Suche abgebrochen wird, und führt dazu, dass das [**ishellfoldersearchablecallback**](ishellfoldersearchablecallback.md) -Schnittstellen Objekt die endgültige Version enthält.</span><span class="sxs-lookup"><span data-stu-id="ac9b3-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac9b3-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ac9b3-120">Requirements</span></span>



| <span data-ttu-id="ac9b3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac9b3-121">Requirement</span></span> | <span data-ttu-id="ac9b3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ac9b3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac9b3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac9b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ac9b3-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac9b3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac9b3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac9b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ac9b3-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac9b3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac9b3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ac9b3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac9b3-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac9b3-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




