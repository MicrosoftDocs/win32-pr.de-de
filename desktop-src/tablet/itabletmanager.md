---
description: Bietet Zugriff auf alle Tablet-PCs, die mit dem Computer verbunden sind.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Itabletmanager-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050534"
---
# <a name="itabletmanager-interface"></a><span data-ttu-id="afc51-103">Itabletmanager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="afc51-103">ITabletManager interface</span></span>

<span data-ttu-id="afc51-104">Bietet Zugriff auf alle Tablet-PCs, die mit dem Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="afc51-104">Provides access to all of the tablets attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="afc51-105">Member</span><span class="sxs-lookup"><span data-stu-id="afc51-105">Members</span></span>

<span data-ttu-id="afc51-106">Die **itabletmanager** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="afc51-106">The **ITabletManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="afc51-107">**Itabletmanager** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="afc51-107">**ITabletManager** also has these types of members:</span></span>

-   [<span data-ttu-id="afc51-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="afc51-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="afc51-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="afc51-109">Methods</span></span>

<span data-ttu-id="afc51-110">Die **itabletmanager** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="afc51-110">The **ITabletManager** interface has these methods.</span></span>



| <span data-ttu-id="afc51-111">Methode</span><span class="sxs-lookup"><span data-stu-id="afc51-111">Method</span></span>                                                  | <span data-ttu-id="afc51-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afc51-112">Description</span></span>                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| <span data-ttu-id="afc51-113">[**Gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="afc51-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span></span>           | <span data-ttu-id="afc51-114">Ruft das angegebene Tablet-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="afc51-114">Retrieves the specified tablet object.</span></span><br/>                  |
| [<span data-ttu-id="afc51-115">**Gettabletcount**</span><span class="sxs-lookup"><span data-stu-id="afc51-115">**GetTabletCount**</span></span>](itabletmanager-gettabletcount.md) | <span data-ttu-id="afc51-116">Ruft die Anzahl der Tablets ab, die an das System angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="afc51-116">Retrieves the number of tablets attached to the system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="afc51-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afc51-117">Remarks</span></span>

<span data-ttu-id="afc51-118">Entwickler sollten diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="afc51-118">Developers should not use this interface.</span></span>

<span data-ttu-id="afc51-119">Der folgende Code zeigt, wie die **itabletmanager** -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="afc51-119">The following code shows how the **ITabletManager** interface is implemented.</span></span>

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

<span data-ttu-id="afc51-120">[**Cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der Klassen-ID "CLSID \_ tabletmanagers" aufrufen und dann " [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) " aufrufen, um einen Zeiger auf die **itabletmanager-Schnittstelle** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="afc51-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class ID of CLSID\_TabletManagerS, and then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the **ITabletManager Interface**.</span></span> <span data-ttu-id="afc51-121">Die GUID "CLSID \_ tabletmanagers" ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="afc51-121">The CLSID\_TabletManagerS GUID is defined as follows:</span></span>

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a><span data-ttu-id="afc51-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afc51-122">Requirements</span></span>



| <span data-ttu-id="afc51-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc51-123">Requirement</span></span> | <span data-ttu-id="afc51-124">Wert</span><span class="sxs-lookup"><span data-stu-id="afc51-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc51-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc51-125">Minimum supported client</span></span><br/> | <span data-ttu-id="afc51-126">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc51-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="afc51-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc51-127">Minimum supported server</span></span><br/> | <span data-ttu-id="afc51-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="afc51-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="afc51-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="afc51-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="afc51-130"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="afc51-130"><dt>Wisptis.exe</dt></span></span> </dl> |



 

