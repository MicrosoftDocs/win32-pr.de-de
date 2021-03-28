---
description: Macht Methoden verfügbar, mit denen ein Shellordner verschiedene Ansichten für seinen Inhalt unterstützt (verschiedene hierarchische Layouts der Daten).
title: Ishellfolderviewtype-Schnittstelle
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
ms.openlocfilehash: 1440b6d14950ad70d2c76168b28bb1077b19b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042242"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="20b4a-103">Ishellfolderviewtype-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="20b4a-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="20b4a-104">Macht Methoden verfügbar, mit denen ein Shellordner verschiedene Ansichten für seinen Inhalt unterstützt (verschiedene hierarchische Layouts der Daten).</span><span class="sxs-lookup"><span data-stu-id="20b4a-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="20b4a-105">Member</span><span class="sxs-lookup"><span data-stu-id="20b4a-105">Members</span></span>

<span data-ttu-id="20b4a-106">Die **ishellfolderviewtype** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="20b4a-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="20b4a-107">**Ishellfolderviewtype** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="20b4a-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="20b4a-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="20b4a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="20b4a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="20b4a-109">Methods</span></span>

<span data-ttu-id="20b4a-110">Die **ishellfolderviewtype** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="20b4a-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="20b4a-111">Methode</span><span class="sxs-lookup"><span data-stu-id="20b4a-111">Method</span></span>                                                                      | <span data-ttu-id="20b4a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20b4a-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20b4a-113">**Enumsichten**</span><span class="sxs-lookup"><span data-stu-id="20b4a-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="20b4a-114">Ruft einen Enumerator ab, der eine PIDL für jede erweiterte Ansicht zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="20b4a-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="20b4a-115">**Getdefaultviewname**</span><span class="sxs-lookup"><span data-stu-id="20b4a-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="20b4a-116">Ruft den Namen der Standardansicht ab.</span><span class="sxs-lookup"><span data-stu-id="20b4a-116">Gets the name of the default view.</span></span> <span data-ttu-id="20b4a-117">Rufen Sie [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um die Namen der anderen Sichten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="20b4a-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="20b4a-118">**Getviewtypeproperties**</span><span class="sxs-lookup"><span data-stu-id="20b4a-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="20b4a-119">Ruft die Eigenschaften der Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="20b4a-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="20b4a-120">**Translateviewpidl**</span><span class="sxs-lookup"><span data-stu-id="20b4a-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="20b4a-121">Rekonstruiert eine PIDL aus einer hierarchischen Darstellung des shellordners in eine andere Darstellung.</span><span class="sxs-lookup"><span data-stu-id="20b4a-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="20b4a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20b4a-122">Remarks</span></span>

<span data-ttu-id="20b4a-123">Dieser Enumerator gibt pidls zurück, bei denen es sich um besondere ausgeblendete Ordner auf der obersten Ebene des shellordners handelt, die ansonsten nicht aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="20b4a-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="20b4a-124">Die Standardansicht ist die Standardansicht, die im Shellordner normal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="20b4a-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="20b4a-125">Diese Schnittstelle ist in keiner öffentlichen Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="20b4a-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="20b4a-126">Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die zugehörigen Methoden zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="20b4a-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderViewType Methods _*_

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList _*ppenum) PURE;

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



## <a name="requirements"></a><span data-ttu-id="20b4a-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="20b4a-127">Requirements</span></span>



| <span data-ttu-id="20b4a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20b4a-128">Requirement</span></span> | <span data-ttu-id="20b4a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="20b4a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20b4a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20b4a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="20b4a-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20b4a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="20b4a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20b4a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="20b4a-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20b4a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="20b4a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="20b4a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b4a-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b4a-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
