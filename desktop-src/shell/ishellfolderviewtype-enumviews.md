---
description: Ruft einen Enumerator ab, der für jede erweiterte Ansicht einen Zeiger auf eine Element Bezeichner Liste (PIDL) zurückgibt.
title: 'Ishellfolderviewtype:: enumviews-Methode'
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
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993823"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="e4c03-103">Ishellfolderviewtype:: enumviews-Methode</span><span class="sxs-lookup"><span data-stu-id="e4c03-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="e4c03-104">Ruft einen Enumerator ab, der für jede erweiterte Ansicht einen Zeiger auf eine Element Bezeichner Liste (PIDL) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e4c03-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4c03-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="e4c03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c03-107">*grfFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4c03-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c03-108">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="e4c03-108">Type: **ULONG**</span></span>

<span data-ttu-id="e4c03-109">Flags, die angeben, welche Elemente in die-Enumeration eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4c03-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="e4c03-110">Eine Liste möglicher Werte finden Sie unter dem Enumerationstyp " [**shcontf**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) ".</span><span class="sxs-lookup"><span data-stu-id="e4c03-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="e4c03-111">Dieser Parameter kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c03-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="e4c03-112">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4c03-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c03-113">Typ: **[ **ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4c03-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="e4c03-114">Die Adresse einer Zeiger Variablen vom Typ [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) , die den Enumerator empfängt.</span><span class="sxs-lookup"><span data-stu-id="e4c03-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c03-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4c03-115">Return value</span></span>

<span data-ttu-id="e4c03-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e4c03-116">Type: **HRESULT**</span></span>

<span data-ttu-id="e4c03-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e4c03-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4c03-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4c03-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4c03-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4c03-119">Remarks</span></span>

<span data-ttu-id="e4c03-120">Sichten werden dem Benutzer als ausgeblendete Ordner aus dem Stammverzeichnis (dargestellt durch pidls) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e4c03-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="e4c03-121">Wenn dies erforderlich ist, wird die Standardansicht (aus dem Stamm Ordner) als **null**-oder leere PIDL dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e4c03-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c03-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e4c03-122">Requirements</span></span>



| <span data-ttu-id="e4c03-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4c03-123">Requirement</span></span> | <span data-ttu-id="e4c03-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e4c03-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c03-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4c03-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c03-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4c03-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e4c03-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4c03-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c03-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4c03-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4c03-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e4c03-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c03-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c03-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




