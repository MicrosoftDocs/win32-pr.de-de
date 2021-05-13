---
description: Ruft einen Enumerator ab, der einen Zeiger auf eine Elementbezeichnerliste (PIDL) für jede erweiterte Ansicht zurückgibt.
title: IShellFolderViewType::EnumViews-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842771"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="9120f-103">IShellFolderViewType::EnumViews-Methode</span><span class="sxs-lookup"><span data-stu-id="9120f-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="9120f-104">Ruft einen Enumerator ab, der einen Zeiger auf eine Elementbezeichnerliste (PIDL) für jede erweiterte Ansicht zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9120f-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="9120f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9120f-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="9120f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9120f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9120f-107">*grfFlags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9120f-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9120f-108">Typ: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="9120f-108">Type: **ULONG**</span></span>

<span data-ttu-id="9120f-109">Flags, die angeben, welche Elemente in die Enumeration eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9120f-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="9120f-110">Eine Liste der möglichen Werte finden Sie unter [**SHCONTF-Enumerationstyp.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf)</span><span class="sxs-lookup"><span data-stu-id="9120f-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="9120f-111">Dieser Parameter kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="9120f-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="9120f-112">*ppenum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9120f-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9120f-113">Typ: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="9120f-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="9120f-114">Die Adresse einer Zeigervariable vom Typ [**IEnumIDList,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) die den Enumerator empfängt.</span><span class="sxs-lookup"><span data-stu-id="9120f-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9120f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9120f-115">Return value</span></span>

<span data-ttu-id="9120f-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9120f-116">Type: **HRESULT**</span></span>

<span data-ttu-id="9120f-117">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9120f-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9120f-118">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9120f-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9120f-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9120f-119">Remarks</span></span>

<span data-ttu-id="9120f-120">Ansichten werden dem Benutzer als ausgeblendete Ordner außerhalb des Stammverzeichnisses (dargestellt durch PIDLs) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9120f-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="9120f-121">Bei Bedarf wird die Standardansicht (außerhalb des Stammordners) als **NULL** oder als leere PIDL dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9120f-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9120f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9120f-122">Requirements</span></span>



| <span data-ttu-id="9120f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9120f-123">Requirement</span></span> | <span data-ttu-id="9120f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9120f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9120f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9120f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9120f-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9120f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9120f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9120f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9120f-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9120f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9120f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9120f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9120f-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9120f-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




