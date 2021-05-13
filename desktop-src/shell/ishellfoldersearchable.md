---
description: Macht Methoden verfügbar, mit denen eine Shellerweiterung einen durchsuchbaren Namespace bereitstellen kann.
title: IShellFolderSearchable-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 6daa00e6821833d783aefa95be23b7b8de769907
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842831"
---
# <a name="ishellfoldersearchable-interface"></a><span data-ttu-id="8f1d4-103">IShellFolderSearchable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8f1d4-103">IShellFolderSearchable interface</span></span>

<span data-ttu-id="8f1d4-104">Macht Methoden verfügbar, mit denen eine Shellerweiterung einen durchsuchbaren Namespace bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-104">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span>

## <a name="members"></a><span data-ttu-id="8f1d4-105">Member</span><span class="sxs-lookup"><span data-stu-id="8f1d4-105">Members</span></span>

<span data-ttu-id="8f1d4-106">Die **IShellFolderSearchable-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="8f1d4-106">The **IShellFolderSearchable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8f1d4-107">**IShellFolderSearchable** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="8f1d4-107">**IShellFolderSearchable** also has these types of members:</span></span>

-   [<span data-ttu-id="8f1d4-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f1d4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8f1d4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f1d4-109">Methods</span></span>

<span data-ttu-id="8f1d4-110">Die **IShellFolderSearchable-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-110">The **IShellFolderSearchable** interface has these methods.</span></span>



| <span data-ttu-id="8f1d4-111">Methode</span><span class="sxs-lookup"><span data-stu-id="8f1d4-111">Method</span></span>                                                                | <span data-ttu-id="8f1d4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f1d4-112">Description</span></span>                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="8f1d4-113">**CancelAsyncSearch**</span><span class="sxs-lookup"><span data-stu-id="8f1d4-113">**CancelAsyncSearch**</span></span>](ishellfoldersearchable-cancelasyncsearch.md) | <span data-ttu-id="8f1d4-114">Startet den Prozess des Abbrechens einer ausstehenden asynchronen Suche.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-114">Begins the process of canceling a pending asynchronous search.</span></span><br/> |
| [<span data-ttu-id="8f1d4-115">**Findstring**</span><span class="sxs-lookup"><span data-stu-id="8f1d4-115">**FindString**</span></span>](ishellfoldersearchable-findstring.md)               | <span data-ttu-id="8f1d4-116">Beginnt eine Suche nach einer angegebenen Suchzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-116">Begins a search for a specified search string.</span></span><br/>                 |
| [<span data-ttu-id="8f1d4-117">**InvalidateSearch**</span><span class="sxs-lookup"><span data-stu-id="8f1d4-117">**InvalidateSearch**</span></span>](ishellfoldersearchable-invalidatesearch.md)   | <span data-ttu-id="8f1d4-118">Macht diese PIDL zu einem ungültigen Teil des Shellordners.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-118">Makes this PIDL an invalid portion of the Shell folder.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="8f1d4-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f1d4-119">Remarks</span></span>

<span data-ttu-id="8f1d4-120">Diese Schnittstelle ist in öffentlichen Headerdateien nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-120">This interface is not defined in any public header files.</span></span> <span data-ttu-id="8f1d4-121">Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die Methoden zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-121">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchable methods ***

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD *pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="8f1d4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f1d4-122">Requirements</span></span>



| <span data-ttu-id="8f1d4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f1d4-123">Requirement</span></span> | <span data-ttu-id="8f1d4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1d4-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f1d4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8f1d4-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f1d4-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8f1d4-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f1d4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8f1d4-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f1d4-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8f1d4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8f1d4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f1d4-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f1d4-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
