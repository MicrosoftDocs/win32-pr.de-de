---
description: Macht Rückruf Routinen zum Überwachen des Suchprozesses verfügbar.
title: Ishellfoldersearchablecallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: aac648861f3bf9dc5ae8fdcc7173792e427b234f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993822"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="4aae5-103">Ishellfoldersearchablecallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4aae5-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="4aae5-104">Macht Rückruf Routinen zum Überwachen des Suchprozesses verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4aae5-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="4aae5-105">Member</span><span class="sxs-lookup"><span data-stu-id="4aae5-105">Members</span></span>

<span data-ttu-id="4aae5-106">Die **ishellfoldersearchablecallback** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4aae5-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4aae5-107">**Ishellfoldersearchablecallback** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4aae5-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="4aae5-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="4aae5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4aae5-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="4aae5-109">Methods</span></span>

<span data-ttu-id="4aae5-110">Die **ishellfoldersearchablecallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4aae5-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="4aae5-111">Methode</span><span class="sxs-lookup"><span data-stu-id="4aae5-111">Method</span></span>                                                      | <span data-ttu-id="4aae5-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aae5-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="4aae5-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="4aae5-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="4aae5-114">Gibt an, dass eine Suche gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4aae5-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="4aae5-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="4aae5-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="4aae5-116">Gibt an, dass eine Suche abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4aae5-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4aae5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aae5-117">Remarks</span></span>

<span data-ttu-id="4aae5-118">Diese Schnittstelle ist in keinen öffentlichen Header Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="4aae5-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="4aae5-119">Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die zugehörigen Methoden zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="4aae5-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchableCallback Methods _**

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="4aae5-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4aae5-120">Requirements</span></span>



| <span data-ttu-id="4aae5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4aae5-121">Requirement</span></span> | <span data-ttu-id="4aae5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4aae5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aae5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4aae5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4aae5-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aae5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4aae5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4aae5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4aae5-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aae5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4aae5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4aae5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aae5-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aae5-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
