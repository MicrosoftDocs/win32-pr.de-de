---
title: ISOFT kbd-Methode für die Methode "deesoftkeyboardlayoutfromresource" ("Soft-BDC. h")
description: Die Methode isoftkbd kreatesoftkeybboardlayoutfromresource erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Kreatesoftkeyboardlayoutfromresource-Methode Text Dienst-Framework
- Kreatesoftkeyboardlayoutfromresource-Methode Text Dienst Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, Methode "kreatesoftkeyboardlayoutfromresource"
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342641"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a><span data-ttu-id="ae179-106">ISOFT kbd:: kreatesoftkeyboardlayoutfromresource-Methode</span><span class="sxs-lookup"><span data-stu-id="ae179-106">ISoftKbd::CreateSoftKeyboardLayoutFromResource method</span></span>

<span data-ttu-id="ae179-107">Die **isoftkbd:: deesoftkeybboardlayoutfromresource** -Methode erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="ae179-107">The **ISoftKbd::CreateSoftKeybboardLayoutFromResource** method creates a soft keyboard layout from the specified resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae179-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae179-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="ae179-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae179-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae179-110">*lpszresfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae179-110">*lpszResFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae179-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der Ressourcen Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="ae179-111">Pointer to a zero-terminated string indicating the name of the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="ae179-112">*lpszrestype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae179-112">*lpszResType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae179-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Typ der Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="ae179-113">Pointer to a zero-terminated string indicating the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="ae179-114">*lpszxmlresstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae179-114">*lpszXMLResString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae179-115">Zeiger auf eine mit NULL endenden Zeichenfolge, die die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ae179-115">Pointer to a zero-terminated string identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ae179-116">*lpdwlayoutcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae179-116">*lpdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae179-117">Ein Zeiger auf den Puffer, in dem diese Methode ein weiches Tastaturlayout-Cookie abruft.</span><span class="sxs-lookup"><span data-stu-id="ae179-117">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae179-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae179-118">Return value</span></span>

<span data-ttu-id="ae179-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ae179-119">This method can return one of these values.</span></span>



| <span data-ttu-id="ae179-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ae179-120">Value</span></span>                                                                                        | <span data-ttu-id="ae179-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae179-121">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ae179-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae179-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ae179-123">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ae179-123">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="ae179-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ae179-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ae179-125">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ae179-125">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ae179-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae179-126">Requirements</span></span>



| <span data-ttu-id="ae179-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae179-127">Requirement</span></span> | <span data-ttu-id="ae179-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ae179-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae179-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae179-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ae179-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae179-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ae179-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae179-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ae179-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae179-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ae179-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ae179-133">Redistributable</span></span><br/>          | <span data-ttu-id="ae179-134">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae179-134">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ae179-135">Header</span><span class="sxs-lookup"><span data-stu-id="ae179-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae179-136"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae179-136"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ae179-137">IDL</span><span class="sxs-lookup"><span data-stu-id="ae179-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae179-138"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae179-138"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ae179-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ae179-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae179-140"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae179-140"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae179-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae179-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae179-142">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="ae179-142">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="ae179-143">**Iweichkbd:: erkreatesoftkeyboardlayoutfromxmlfile**</span><span class="sxs-lookup"><span data-stu-id="ae179-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[<span data-ttu-id="ae179-144">**Iweichkbd:: ShowSoft Keyboard**</span><span class="sxs-lookup"><span data-stu-id="ae179-144">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





