---
description: Ruft den Namen der Standardansicht ab. Rufen Sie GetDisplayNameOf auf, um die Namen der anderen Ansichten abzurufen.
title: IShellFolderViewType::GetDefaultViewName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842761"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="d7ad7-104">IShellFolderViewType::GetDefaultViewName-Methode</span><span class="sxs-lookup"><span data-stu-id="d7ad7-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="d7ad7-105">Ruft den Namen der Standardansicht ab.</span><span class="sxs-lookup"><span data-stu-id="d7ad7-105">Gets the name of the default view.</span></span> <span data-ttu-id="d7ad7-106">Rufen [**Sie GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um die Namen der anderen Ansichten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7ad7-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ad7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7ad7-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="d7ad7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7ad7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ad7-109">*uFlags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d7ad7-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ad7-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d7ad7-110">Type: **DWORD**</span></span>

<span data-ttu-id="d7ad7-111">Optionale Flags; sollte auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d7ad7-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad7-112">*ppwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d7ad7-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ad7-113">Typ: **LPWSTR \***</span><span class="sxs-lookup"><span data-stu-id="d7ad7-113">Type: **LPWSTR\***</span></span>

<span data-ttu-id="d7ad7-114">Die Adresse eines Zeichenfolgenzeigers, der den Standardansichtsnamen empfängt.</span><span class="sxs-lookup"><span data-stu-id="d7ad7-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="d7ad7-115">Der Arbeitsspeicher für die Zeichenfolge wird mit [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d7ad7-115">The memory for the string is allocated with [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ad7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7ad7-116">Return value</span></span>

<span data-ttu-id="d7ad7-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d7ad7-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d7ad7-118">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ad7-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7ad7-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ad7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ad7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7ad7-120">Requirements</span></span>



| <span data-ttu-id="d7ad7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7ad7-121">Requirement</span></span> | <span data-ttu-id="d7ad7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d7ad7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ad7-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7ad7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ad7-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7ad7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7ad7-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7ad7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ad7-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7ad7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7ad7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d7ad7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7ad7-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7ad7-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




