---
description: Macht Methoden verfügbar, mit denen eine Shellerweiterung einen durchsuchbaren Namespace bereitstellen kann.
title: Ishellfoldersearchable-Schnittstelle
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
ms.openlocfilehash: 1f42b3af012361bfd24c93e03c38e6954eb5326e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977944"
---
# <a name="ishellfoldersearchable-interface"></a><span data-ttu-id="409c3-103">Ishellfoldersearchable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="409c3-103">IShellFolderSearchable interface</span></span>

<span data-ttu-id="409c3-104">Macht Methoden verfügbar, mit denen eine Shellerweiterung einen durchsuchbaren Namespace bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="409c3-104">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span>

## <a name="members"></a><span data-ttu-id="409c3-105">Member</span><span class="sxs-lookup"><span data-stu-id="409c3-105">Members</span></span>

<span data-ttu-id="409c3-106">Die **ishellfoldersearchable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="409c3-106">The **IShellFolderSearchable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="409c3-107">**Ishellfoldersearchable** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="409c3-107">**IShellFolderSearchable** also has these types of members:</span></span>

-   [<span data-ttu-id="409c3-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="409c3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="409c3-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="409c3-109">Methods</span></span>

<span data-ttu-id="409c3-110">Die **ishellfoldersearchable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="409c3-110">The **IShellFolderSearchable** interface has these methods.</span></span>



| <span data-ttu-id="409c3-111">Methode</span><span class="sxs-lookup"><span data-stu-id="409c3-111">Method</span></span>                                                                | <span data-ttu-id="409c3-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="409c3-112">Description</span></span>                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="409c3-113">**Cancelasyncsearch**</span><span class="sxs-lookup"><span data-stu-id="409c3-113">**CancelAsyncSearch**</span></span>](ishellfoldersearchable-cancelasyncsearch.md) | <span data-ttu-id="409c3-114">Startet das Abbrechen einer ausstehenden asynchronen Suche.</span><span class="sxs-lookup"><span data-stu-id="409c3-114">Begins the process of canceling a pending asynchronous search.</span></span><br/> |
| [<span data-ttu-id="409c3-115">**FindString**</span><span class="sxs-lookup"><span data-stu-id="409c3-115">**FindString**</span></span>](ishellfoldersearchable-findstring.md)               | <span data-ttu-id="409c3-116">Startet eine Suche nach einer angegebenen Such Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="409c3-116">Begins a search for a specified search string.</span></span><br/>                 |
| [<span data-ttu-id="409c3-117">**Invalidatesearch**</span><span class="sxs-lookup"><span data-stu-id="409c3-117">**InvalidateSearch**</span></span>](ishellfoldersearchable-invalidatesearch.md)   | <span data-ttu-id="409c3-118">Macht diese PIDL zu einem ungültigen Teil des shellordners.</span><span class="sxs-lookup"><span data-stu-id="409c3-118">Makes this PIDL an invalid portion of the Shell folder.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="409c3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="409c3-119">Remarks</span></span>

<span data-ttu-id="409c3-120">Diese Schnittstelle ist in keinen öffentlichen Header Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="409c3-120">This interface is not defined in any public header files.</span></span> <span data-ttu-id="409c3-121">Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die zugehörigen Methoden zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="409c3-121">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchable methods _*_

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD _pdwFlags,
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



## <a name="requirements"></a><span data-ttu-id="409c3-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="409c3-122">Requirements</span></span>



| <span data-ttu-id="409c3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="409c3-123">Requirement</span></span> | <span data-ttu-id="409c3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="409c3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="409c3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="409c3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="409c3-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="409c3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="409c3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="409c3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="409c3-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="409c3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="409c3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="409c3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="409c3-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="409c3-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
