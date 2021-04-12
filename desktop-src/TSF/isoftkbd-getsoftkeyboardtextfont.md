---
title: ISoftware. getsoft keyboardtextfont-Methode (Software-DC. h)
description: Die isoftkbd getsoftkeyboardtextfont-Methode ruft die von einer Soft Tastatur verwendete Text Schriftart ab.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Getsoft keyboardtextfont-Methode Text Services-Framework
- Getsoft keyboardtextfont-Methode Text Services-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, getsoft keyboardtextfont-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105249"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a><span data-ttu-id="05dd3-106">Iweichkbd:: getsoft keyboardtextfont-Methode</span><span class="sxs-lookup"><span data-stu-id="05dd3-106">ISoftKbd::GetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="05dd3-107">Die **isoftkbd:: getsoftkeyboardtextfont** -Methode ruft die von einer Soft Tastatur verwendete Text Schriftart ab.</span><span class="sxs-lookup"><span data-stu-id="05dd3-107">The **ISoftKbd::GetSoftKeyboardTextFont** method retrieves the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="05dd3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="05dd3-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="05dd3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="05dd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05dd3-110">*plogfont* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="05dd3-110">*pLogFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05dd3-111">Ein Zeiger auf einen Puffer, in dem diese Methode eine [**logfontw**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur abruft, die die Text Schriftart für die weiche Tastatur definiert.</span><span class="sxs-lookup"><span data-stu-id="05dd3-111">Pointer to a buffer in which this method retrieves a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05dd3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05dd3-112">Return value</span></span>

<span data-ttu-id="05dd3-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="05dd3-113">This method can return one of these values.</span></span>



| <span data-ttu-id="05dd3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="05dd3-114">Value</span></span>                                                                                        | <span data-ttu-id="05dd3-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05dd3-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="05dd3-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05dd3-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="05dd3-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="05dd3-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="05dd3-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="05dd3-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="05dd3-119">Der *plogfont* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="05dd3-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05dd3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05dd3-120">Requirements</span></span>



| <span data-ttu-id="05dd3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05dd3-121">Requirement</span></span> | <span data-ttu-id="05dd3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="05dd3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05dd3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05dd3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="05dd3-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05dd3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05dd3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05dd3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="05dd3-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05dd3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="05dd3-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="05dd3-127">Redistributable</span></span><br/>          | <span data-ttu-id="05dd3-128">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="05dd3-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="05dd3-129">Header</span><span class="sxs-lookup"><span data-stu-id="05dd3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="05dd3-130"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="05dd3-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="05dd3-131">IDL</span><span class="sxs-lookup"><span data-stu-id="05dd3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05dd3-132"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05dd3-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="05dd3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="05dd3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05dd3-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05dd3-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05dd3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05dd3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05dd3-136">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="05dd3-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="05dd3-137">**Icdkbd:: setsoftware keyboardtextfont**</span><span class="sxs-lookup"><span data-stu-id="05dd3-137">**ISoftKbd::SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

