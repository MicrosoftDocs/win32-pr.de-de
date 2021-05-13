---
description: Macht Methoden verfügbar, die es einem Shell-Ordner ermöglichen, verschiedene Ansichten des Inhalts (unterschiedliche hierarchische Layouts seiner Daten) zu unterstützen.
title: IShellFolderViewType-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: f3ccb4073d59e0ebe9b840bd6f8f592f463e1e46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842691"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="24db3-103">IShellFolderViewType-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="24db3-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="24db3-104">Macht Methoden verfügbar, die es einem Shell-Ordner ermöglichen, verschiedene Ansichten des Inhalts (unterschiedliche hierarchische Layouts seiner Daten) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="24db3-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="24db3-105">Member</span><span class="sxs-lookup"><span data-stu-id="24db3-105">Members</span></span>

<span data-ttu-id="24db3-106">Die **IShellFolderViewType-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="24db3-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="24db3-107">**IShellFolderViewType** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="24db3-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="24db3-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="24db3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="24db3-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="24db3-109">Methods</span></span>

<span data-ttu-id="24db3-110">Die **IShellFolderViewType-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="24db3-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="24db3-111">Methode</span><span class="sxs-lookup"><span data-stu-id="24db3-111">Method</span></span>                                                                      | <span data-ttu-id="24db3-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24db3-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24db3-113">**EnumViews**</span><span class="sxs-lookup"><span data-stu-id="24db3-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="24db3-114">Ruft einen Enumerator ab, der eine PIDL für jede erweiterte Ansicht zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="24db3-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="24db3-115">**GetDefaultViewName**</span><span class="sxs-lookup"><span data-stu-id="24db3-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="24db3-116">Ruft den Namen der Standardansicht ab.</span><span class="sxs-lookup"><span data-stu-id="24db3-116">Gets the name of the default view.</span></span> <span data-ttu-id="24db3-117">Rufen [**Sie IShellFolder::GetDisplayNameOf auf,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) um die Namen der anderen Ansichten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="24db3-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="24db3-118">**GetViewTypeProperties**</span><span class="sxs-lookup"><span data-stu-id="24db3-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="24db3-119">Ruft die Eigenschaften der Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="24db3-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="24db3-120">**TranslateViewPidl**</span><span class="sxs-lookup"><span data-stu-id="24db3-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="24db3-121">Rekonstruiert eine PIDL aus einer hierarchischen Darstellung des Shellordners in einer anderen Darstellung.</span><span class="sxs-lookup"><span data-stu-id="24db3-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="24db3-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24db3-122">Remarks</span></span>

<span data-ttu-id="24db3-123">Dieser Enumerator gibt PIDLs zurück, bei denen es sich um spezielle ausgeblendete Ordner auf der obersten Ebene des Shellordners handelt, die andernfalls nicht aufzählt werden.</span><span class="sxs-lookup"><span data-stu-id="24db3-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="24db3-124">Die Standardansicht ist die Ansicht, die der Shellordner normal anzeigt.</span><span class="sxs-lookup"><span data-stu-id="24db3-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="24db3-125">Diese Schnittstelle ist in einer öffentlichen Headerdatei nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="24db3-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="24db3-126">Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die Methoden zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="24db3-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderViewType Methods ***

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList **ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a><span data-ttu-id="24db3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24db3-127">Requirements</span></span>



| <span data-ttu-id="24db3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24db3-128">Requirement</span></span> | <span data-ttu-id="24db3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="24db3-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24db3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24db3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="24db3-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24db3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="24db3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24db3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="24db3-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24db3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="24db3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="24db3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24db3-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24db3-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
