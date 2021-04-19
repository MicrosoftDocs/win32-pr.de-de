---
title: Querylayoutortipstringuserreg-Funktion
description: Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen mit dem angegebenen Registrierungs Pfad darstellt.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- Querylayoutortipstringuserreg-Funktion Text Dienst-Framework
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342464"
---
# <a name="querylayoutortipstringuserreg-function"></a><span data-ttu-id="22700-104">Querylayoutortipstringuserreg-Funktion</span><span class="sxs-lookup"><span data-stu-id="22700-104">QueryLayoutOrTipStringUserReg function</span></span>

<span data-ttu-id="22700-105">Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen mit dem angegebenen Registrierungs Pfad darstellt.</span><span class="sxs-lookup"><span data-stu-id="22700-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list of the specified registry path.</span></span>

## <a name="syntax"></a><span data-ttu-id="22700-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="22700-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="22700-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22700-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22700-108">*pszuserreg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22700-108">*pszUserReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22700-109">Der Registrierungs Pfad des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="22700-109">The registry path of the user.</span></span> <span data-ttu-id="22700-110">Wenn dieser Parameter **null** ist, wird der aktuelle HKEY- \_ \_ Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="22700-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="22700-111">*pszsystemreg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22700-111">*pszSystemReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22700-112">Der Registrierungs Pfad des Systems.</span><span class="sxs-lookup"><span data-stu-id="22700-112">The registry path of the system.</span></span> <span data-ttu-id="22700-113">Wenn dieser Parameter **null** ist, wird HKEY \_ local \_ Machine \\ System verwendet.</span><span class="sxs-lookup"><span data-stu-id="22700-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="22700-114">*pszsoftwarerereg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22700-114">*pszSoftwareReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22700-115">Der Registrierungs Pfad der Software.</span><span class="sxs-lookup"><span data-stu-id="22700-115">The registry path of the software.</span></span> <span data-ttu-id="22700-116">Wenn dieser Parameter **null** ist, wird die lokale HKEY- \_ \_ Computer \\ Software verwendet.</span><span class="sxs-lookup"><span data-stu-id="22700-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="22700-117">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22700-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22700-118">Eine Zeichenfolge, die eine Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.</span><span class="sxs-lookup"><span data-stu-id="22700-118">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="22700-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22700-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22700-120">Diese Angabe muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="22700-120">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22700-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22700-121">Return value</span></span>

<span data-ttu-id="22700-122">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22700-122">This function can return one of these values.</span></span>



| <span data-ttu-id="22700-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22700-123">Return code</span></span>                                                                                  | <span data-ttu-id="22700-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22700-124">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22700-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22700-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="22700-126">Alle in **PSZ** definierten Layouts oder Profile sind gültig.</span><span class="sxs-lookup"><span data-stu-id="22700-126">All layouts or profiles defined in **psz** are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="22700-127"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="22700-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="22700-128">Mindestens eines der in **PSZ** definierten Layouts oder Profile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="22700-128">One or more of the layouts or profiles defined in **psz** are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22700-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22700-129">Remarks</span></span>

<span data-ttu-id="22700-130">Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22700-130">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="22700-131">Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="22700-131">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="22700-132">Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="22700-132">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="22700-133">Das Zeichen folgen Format der Layoutliste lautet:</span><span class="sxs-lookup"><span data-stu-id="22700-133">The string format of the layout list is:</span></span>

<span data-ttu-id="22700-134"><langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="22700-134"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="22700-135">Das Zeichen folgen Format der Text Dienst Profil Liste lautet:</span><span class="sxs-lookup"><span data-stu-id="22700-135">The string format of the text service profile list is:</span></span>

<span data-ttu-id="22700-136"><langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="22700-136"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="22700-137">Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="22700-137">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="22700-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22700-138">Requirements</span></span>



| <span data-ttu-id="22700-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22700-139">Requirement</span></span> | <span data-ttu-id="22700-140">Wert</span><span class="sxs-lookup"><span data-stu-id="22700-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22700-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22700-141">Minimum supported client</span></span><br/> | <span data-ttu-id="22700-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22700-142">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="22700-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22700-143">Minimum supported server</span></span><br/> | <span data-ttu-id="22700-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22700-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="22700-145">DLL</span><span class="sxs-lookup"><span data-stu-id="22700-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22700-146"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22700-146"><dt>Input.dll</dt></span></span> </dl> |



 

