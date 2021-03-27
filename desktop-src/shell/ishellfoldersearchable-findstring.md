---
description: Startet eine Suche nach einer angegebenen Such Zeichenfolge.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Ishellfoldersearchable:: FindString-Methode (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753064"
---
# <a name="ishellfoldersearchablefindstring-method"></a><span data-ttu-id="8b38f-103">Ishellfoldersearchable:: FindString-Methode</span><span class="sxs-lookup"><span data-stu-id="8b38f-103">IShellFolderSearchable::FindString method</span></span>

<span data-ttu-id="8b38f-104">Startet eine Suche nach einer angegebenen Such Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8b38f-104">Begins a search for a specified search string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b38f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b38f-105">Syntax</span></span>


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="8b38f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b38f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b38f-107">*pwsztarget* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b38f-107">*pwszTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b38f-108">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="8b38f-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="8b38f-109">Ein Zeiger auf eine Zeichenfolge, die das Schlüsselwort für die Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="8b38f-109">A pointer to a string that specifies the search keyword.</span></span>

</dd> <dt>

<span data-ttu-id="8b38f-110">*pdwflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b38f-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b38f-111">Typ: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="8b38f-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="8b38f-112">Zurzeit sind keine Flags definiert. Legen Sie auf _ \* NULL \* \* fest.</span><span class="sxs-lookup"><span data-stu-id="8b38f-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="8b38f-113">*punkonasyncsearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b38f-113">*punkOnAsyncSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b38f-114">Typ: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="8b38f-114">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="8b38f-115">Ein Zeiger auf ein Objekt vom Typ [_ *IUnknown* \*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="8b38f-115">A pointer to an object of type [_ *IUnknown*\*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="8b38f-116">Dieses Objekt muss die [**ishellfoldersearchablecallback**](ishellfoldersearchablecallback.md) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8b38f-116">This object must support the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface.</span></span> <span data-ttu-id="8b38f-117">Auf **null** festgelegt, wenn kein Rückruf erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8b38f-117">Set to **NULL** if no callback is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="8b38f-118">*ppidlout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b38f-118">*ppidlOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b38f-119">Typ: **lpitemittellist**</span><span class="sxs-lookup"><span data-stu-id="8b38f-119">Type: **LPITEMIDLIST**</span></span>

<span data-ttu-id="8b38f-120">Ein Zeiger auf eine [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur für den Suchordner.</span><span class="sxs-lookup"><span data-stu-id="8b38f-120">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b38f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b38f-121">Return value</span></span>

<span data-ttu-id="8b38f-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b38f-122">Type: **HRESULT**</span></span>

<span data-ttu-id="8b38f-123">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8b38f-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b38f-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b38f-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b38f-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8b38f-125">Requirements</span></span>



| <span data-ttu-id="8b38f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b38f-126">Requirement</span></span> | <span data-ttu-id="8b38f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8b38f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b38f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b38f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8b38f-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b38f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8b38f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b38f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8b38f-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b38f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8b38f-132">Header</span><span class="sxs-lookup"><span data-stu-id="8b38f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b38f-133"><dt>MMC. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b38f-133"><dt>Mmc.h</dt></span></span> </dl>       |
| <span data-ttu-id="8b38f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8b38f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b38f-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b38f-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
