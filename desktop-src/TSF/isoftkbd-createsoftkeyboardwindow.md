---
title: ISOFT kbd-Methode von "samatesoftkeyboardwindow" ("Soft-BDC. h")
description: Mit der isoftkbd-Methode "kreatesoftkeyboardwindow" wird ein vorläufiges Tastatur Fenster erstellt.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- "\"Kreatesoftkeyboardwindow\"-Methode, Text Dienste-Framework"
- Kreatesoftkeyboardwindow-Methode Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, Methode "kreatesoftkeyboardwindow"
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518407"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a><span data-ttu-id="420ad-106">ISOFT kbd:: kreatesoftkeyboardwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="420ad-106">ISoftKbd::CreateSoftKeyboardWindow method</span></span>

<span data-ttu-id="420ad-107">Die **isoftkbd:: kreatesoftkeyboardwindow** -Methode erstellt ein weiches Tastatur Fenster.</span><span class="sxs-lookup"><span data-stu-id="420ad-107">The **ISoftKbd::CreateSoftKeyboardWindow** method creates a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="420ad-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="420ad-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a><span data-ttu-id="420ad-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="420ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="420ad-110">*howner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="420ad-110">*hOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420ad-111">Handle des Fensters, das die weiche Tastatur enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="420ad-111">Handle of the window to contain the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="420ad-112">*TitleBar- \_ Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="420ad-112">*Titlebar\_type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420ad-113">Der Typ der Titelleiste für das weiche Tastatur Fenster.</span><span class="sxs-lookup"><span data-stu-id="420ad-113">Type of title bar for the soft keyboard window.</span></span> <span data-ttu-id="420ad-114">Mögliche Typen werden durch die [**TitleBar- \_ Typenumeration**](titlebar-type.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="420ad-114">Possible types are defined by the [**TITLEBAR\_TYPE**](titlebar-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="420ad-115">*xPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="420ad-115">*xPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420ad-116">Die x-Position der oberen linken Ecke des Soft Tastatur Fensters.</span><span class="sxs-lookup"><span data-stu-id="420ad-116">The x position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="420ad-117">*yPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="420ad-117">*yPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420ad-118">Die y-Position der oberen linken Ecke des Soft Tastatur Fensters.</span><span class="sxs-lookup"><span data-stu-id="420ad-118">The y position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="420ad-119">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="420ad-119">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420ad-120">Die Breite des Soft Tastatur Fensters.</span><span class="sxs-lookup"><span data-stu-id="420ad-120">The width of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="420ad-121">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="420ad-121">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420ad-122">Die Höhe des Soft Tastatur Fensters.</span><span class="sxs-lookup"><span data-stu-id="420ad-122">The height of the soft keyboard window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="420ad-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="420ad-123">Return value</span></span>

<span data-ttu-id="420ad-124">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="420ad-124">This method can return one of these values.</span></span>



| <span data-ttu-id="420ad-125">Wert</span><span class="sxs-lookup"><span data-stu-id="420ad-125">Value</span></span>                                                                                        | <span data-ttu-id="420ad-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="420ad-126">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="420ad-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="420ad-127"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="420ad-128">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="420ad-128">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="420ad-129"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="420ad-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="420ad-130">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="420ad-130">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="420ad-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="420ad-131">Requirements</span></span>



| <span data-ttu-id="420ad-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="420ad-132">Requirement</span></span> | <span data-ttu-id="420ad-133">Wert</span><span class="sxs-lookup"><span data-stu-id="420ad-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="420ad-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="420ad-134">Minimum supported client</span></span><br/> | <span data-ttu-id="420ad-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="420ad-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="420ad-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="420ad-136">Minimum supported server</span></span><br/> | <span data-ttu-id="420ad-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="420ad-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="420ad-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="420ad-138">Redistributable</span></span><br/>          | <span data-ttu-id="420ad-139">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="420ad-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="420ad-140">Header</span><span class="sxs-lookup"><span data-stu-id="420ad-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="420ad-141"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="420ad-141"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="420ad-142">IDL</span><span class="sxs-lookup"><span data-stu-id="420ad-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="420ad-143"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="420ad-143"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="420ad-144">DLL</span><span class="sxs-lookup"><span data-stu-id="420ad-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="420ad-145"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="420ad-145"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="420ad-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="420ad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="420ad-147">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="420ad-147">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="420ad-148">**ISOFT kbd:: kreatesoftkeyboardlayoutfromresource**</span><span class="sxs-lookup"><span data-stu-id="420ad-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[<span data-ttu-id="420ad-149">**ISOFT kbd::D estroysoft keyboardwindow**</span><span class="sxs-lookup"><span data-stu-id="420ad-149">**ISoftKbd::DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[<span data-ttu-id="420ad-150">**Iweichkbd:: ShowSoft Keyboard**</span><span class="sxs-lookup"><span data-stu-id="420ad-150">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[<span data-ttu-id="420ad-151">**TitleBar- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="420ad-151">**TITLEBAR\_TYPE**</span></span>](titlebar-type.md)
</dt> </dl>

 

 





