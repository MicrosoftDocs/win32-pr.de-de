---
description: Rekonstruiert einen Zeiger auf eine Elementbezeichnerliste (PIDL) aus einer hierarchischen Darstellung des Shellordners in einer anderen Darstellung.
title: IShellFolderViewType::TranslateViewPidl-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842671"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="44030-103">IShellFolderViewType::TranslateViewPidl-Methode</span><span class="sxs-lookup"><span data-stu-id="44030-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="44030-104">Rekonstruiert einen Zeiger auf eine Elementbezeichnerliste (PIDL) aus einer hierarchischen Darstellung des Shellordners in einer anderen Darstellung.</span><span class="sxs-lookup"><span data-stu-id="44030-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="44030-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44030-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="44030-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44030-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44030-107">*pidl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="44030-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44030-108">Typ: **PCUIDLIST \_ RELATIVE**</span><span class="sxs-lookup"><span data-stu-id="44030-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="44030-109">Das Array von Element-IDs relativ zum Stammordner.</span><span class="sxs-lookup"><span data-stu-id="44030-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="44030-110">*pidlView* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="44030-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44030-111">Typ: **PCUIDLIST \_ RELATIVE**</span><span class="sxs-lookup"><span data-stu-id="44030-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="44030-112">Spezielle PIDL der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="44030-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="44030-113">*dldlOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="44030-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44030-114">Typ: **PCUIDLIST \_ RELATIVE \***</span><span class="sxs-lookup"><span data-stu-id="44030-114">Type: **PCUIDLIST\_RELATIVE\***</span></span>

<span data-ttu-id="44030-115">Die Adresse einer PIDL-Variablen, die die Übersetzung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="44030-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44030-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44030-116">Return value</span></span>

<span data-ttu-id="44030-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="44030-117">Type: **HRESULT**</span></span>

<span data-ttu-id="44030-118">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="44030-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44030-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44030-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="44030-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44030-120">Remarks</span></span>

<span data-ttu-id="44030-121">Wenn Sie fertig sind, sollten Sie die zurückgegebene PIDL mit [**ILFree frei geben.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)</span><span class="sxs-lookup"><span data-stu-id="44030-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="44030-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44030-122">Requirements</span></span>



| <span data-ttu-id="44030-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44030-123">Requirement</span></span> | <span data-ttu-id="44030-124">Wert</span><span class="sxs-lookup"><span data-stu-id="44030-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44030-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44030-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44030-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44030-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="44030-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44030-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44030-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44030-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="44030-129">DLL</span><span class="sxs-lookup"><span data-stu-id="44030-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44030-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44030-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




