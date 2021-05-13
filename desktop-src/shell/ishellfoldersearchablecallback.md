---
description: Macht Rückrufroutinen verfügbar, um den Suchvorgang zu überwachen.
title: IShellFolderSearchableCallback-Schnittstelle
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
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842781"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="64620-103">IShellFolderSearchableCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="64620-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="64620-104">Macht Rückrufroutinen verfügbar, um den Suchvorgang zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="64620-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="64620-105">Member</span><span class="sxs-lookup"><span data-stu-id="64620-105">Members</span></span>

<span data-ttu-id="64620-106">Die **IShellFolderSearchableCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="64620-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="64620-107">**IShellFolderSearchableCallback** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64620-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="64620-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="64620-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="64620-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="64620-109">Methods</span></span>

<span data-ttu-id="64620-110">Die **IShellFolderSearchableCallback-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="64620-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="64620-111">Methode</span><span class="sxs-lookup"><span data-stu-id="64620-111">Method</span></span>                                                      | <span data-ttu-id="64620-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64620-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="64620-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="64620-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="64620-114">Gibt an, dass eine Suche gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="64620-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="64620-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="64620-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="64620-116">Gibt an, dass eine Suche abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="64620-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="64620-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64620-117">Remarks</span></span>

<span data-ttu-id="64620-118">Diese Schnittstelle ist nicht in öffentlichen Headerdateien definiert.</span><span class="sxs-lookup"><span data-stu-id="64620-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="64620-119">Wenn Sie diese Schnittstelle implementieren möchten, können Sie den folgenden C/C++-Code verwenden, um die zugehörigen Methoden zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="64620-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="64620-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64620-120">Requirements</span></span>



| <span data-ttu-id="64620-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64620-121">Requirement</span></span> | <span data-ttu-id="64620-122">Wert</span><span class="sxs-lookup"><span data-stu-id="64620-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64620-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64620-123">Minimum supported client</span></span><br/> | <span data-ttu-id="64620-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64620-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="64620-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64620-125">Minimum supported server</span></span><br/> | <span data-ttu-id="64620-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64620-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="64620-127">DLL</span><span class="sxs-lookup"><span data-stu-id="64620-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64620-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64620-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
