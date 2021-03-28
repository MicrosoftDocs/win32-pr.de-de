---
description: Ruft den Namen der Standardansicht ab. Rufen Sie GetDisplayNameOf auf, um die Namen der anderen Sichten abzurufen.
title: 'Ishellfolderviewtype:: getdefaultviewname-Methode'
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
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977937"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="86b2f-104">Ishellfolderviewtype:: getdefaultviewname-Methode</span><span class="sxs-lookup"><span data-stu-id="86b2f-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="86b2f-105">Ruft den Namen der Standardansicht ab.</span><span class="sxs-lookup"><span data-stu-id="86b2f-105">Gets the name of the default view.</span></span> <span data-ttu-id="86b2f-106">Rufen Sie [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um die Namen der anderen Sichten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="86b2f-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b2f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="86b2f-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="86b2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="86b2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b2f-109">*uFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86b2f-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b2f-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="86b2f-110">Type: **DWORD**</span></span>

<span data-ttu-id="86b2f-111">Optionale Flags; muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="86b2f-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="86b2f-112">*ppwszname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="86b2f-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86b2f-113">Typ: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="86b2f-113">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="86b2f-114">Die Adresse eines Zeichen folgen Zeigers, der den Standard Ansichts Namen empfängt.</span><span class="sxs-lookup"><span data-stu-id="86b2f-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="86b2f-115">Der Arbeitsspeicher für die Zeichenfolge wird mit [_ *shundup* \*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="86b2f-115">The memory for the string is allocated with [_ *SHStrDup*\*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b2f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86b2f-116">Return value</span></span>

<span data-ttu-id="86b2f-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="86b2f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="86b2f-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="86b2f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86b2f-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="86b2f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b2f-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="86b2f-120">Requirements</span></span>



| <span data-ttu-id="86b2f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86b2f-121">Requirement</span></span> | <span data-ttu-id="86b2f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="86b2f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86b2f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86b2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="86b2f-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86b2f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="86b2f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86b2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="86b2f-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86b2f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="86b2f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="86b2f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86b2f-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86b2f-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




