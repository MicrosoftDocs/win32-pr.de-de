---
title: Querylayoutortipstring-Funktion
description: Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- Querylayoutortipstring-Funktion, Text Dienste-Framework
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342465"
---
# <a name="querylayoutortipstring-function"></a><span data-ttu-id="5b31b-104">Querylayoutortipstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b31b-104">QueryLayoutOrTipString function</span></span>

<span data-ttu-id="5b31b-105">Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b31b-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b31b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b31b-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5b31b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b31b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b31b-108">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b31b-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b31b-109">Eine Zeichenfolge, die eine Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b31b-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="5b31b-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b31b-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b31b-111">Diese Angabe muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="5b31b-111">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b31b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b31b-112">Return value</span></span>

<span data-ttu-id="5b31b-113">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5b31b-113">This function can return one of these values.</span></span>



| <span data-ttu-id="5b31b-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5b31b-114">Return code</span></span>                                                                                  | <span data-ttu-id="5b31b-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b31b-115">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5b31b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5b31b-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5b31b-117">Alle in *PSZ* definierten Layouts oder Profile sind gültig.</span><span class="sxs-lookup"><span data-stu-id="5b31b-117">All layouts or profiles defined in *psz* are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="5b31b-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="5b31b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5b31b-119">Mindestens eines der in *PSZ* definierten Layouts oder Profile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5b31b-119">One or more of the layouts or profiles defined in *psz* are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b31b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b31b-120">Remarks</span></span>

<span data-ttu-id="5b31b-121">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5b31b-121">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="5b31b-122">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5b31b-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="5b31b-123">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="5b31b-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="5b31b-124">Das Zeichen folgen Format der Layoutliste lautet:</span><span class="sxs-lookup"><span data-stu-id="5b31b-124">The string format of the layout list is:</span></span>

<span data-ttu-id="5b31b-125"><langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="5b31b-125"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="5b31b-126">Das Zeichen folgen Format der Text Dienst Profil Liste lautet:</span><span class="sxs-lookup"><span data-stu-id="5b31b-126">The string format of the text service profile list is:</span></span>

<span data-ttu-id="5b31b-127"><langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="5b31b-127"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="5b31b-128">Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="5b31b-128">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="5b31b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b31b-129">Requirements</span></span>



| <span data-ttu-id="5b31b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b31b-130">Requirement</span></span> | <span data-ttu-id="5b31b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5b31b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b31b-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b31b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5b31b-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b31b-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5b31b-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b31b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5b31b-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b31b-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b31b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5b31b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b31b-137"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b31b-137"><dt>Input.dll</dt></span></span> </dl> |



 

