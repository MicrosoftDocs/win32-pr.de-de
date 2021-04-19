---
title: Icdkbd setsoft keyboardtextfont-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardtextfont-Methode legt die Text Schriftart fest, die von einer Soft Tastatur verwendet wird.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Setsoft keyboardtextfont-Methode Text Services-Framework
- Setsoft keyboardtextfont-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardtextfont-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342859"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a><span data-ttu-id="23234-106">ISOFT kbd:: setsoft keyboardtextfont-Methode</span><span class="sxs-lookup"><span data-stu-id="23234-106">ISoftKbd::SetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="23234-107">Die **isoftkbd:: setsoftkeyboardtextfont** -Methode legt die Text Schriftart fest, die von einer Soft Tastatur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="23234-107">The **ISoftKbd::SetSoftKeyboardTextFont** method sets the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="23234-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="23234-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="23234-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="23234-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23234-110">*plogfont* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23234-110">*pLogFont* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23234-111">Zeiger auf eine [**logfontw**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die die Text Schriftart für die weiche Tastatur definiert.</span><span class="sxs-lookup"><span data-stu-id="23234-111">Pointer to a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23234-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23234-112">Return value</span></span>

<span data-ttu-id="23234-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="23234-113">This method can return one of these values.</span></span>



| <span data-ttu-id="23234-114">Wert</span><span class="sxs-lookup"><span data-stu-id="23234-114">Value</span></span>                                                                                        | <span data-ttu-id="23234-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23234-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="23234-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="23234-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="23234-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="23234-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="23234-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="23234-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="23234-119">Der *plogfont* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="23234-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="23234-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23234-120">Requirements</span></span>



| <span data-ttu-id="23234-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23234-121">Requirement</span></span> | <span data-ttu-id="23234-122">Wert</span><span class="sxs-lookup"><span data-stu-id="23234-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23234-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23234-123">Minimum supported client</span></span><br/> | <span data-ttu-id="23234-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23234-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="23234-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23234-125">Minimum supported server</span></span><br/> | <span data-ttu-id="23234-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23234-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="23234-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="23234-127">Redistributable</span></span><br/>          | <span data-ttu-id="23234-128">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="23234-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="23234-129">Header</span><span class="sxs-lookup"><span data-stu-id="23234-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="23234-130"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="23234-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="23234-131">IDL</span><span class="sxs-lookup"><span data-stu-id="23234-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23234-132"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23234-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="23234-133">DLL</span><span class="sxs-lookup"><span data-stu-id="23234-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23234-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23234-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23234-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23234-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23234-136">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="23234-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="23234-137">**Iweichkbd:: getsoftware keyboardtextfont**</span><span class="sxs-lookup"><span data-stu-id="23234-137">**ISoftKbd::GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

