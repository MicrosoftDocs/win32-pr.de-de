---
title: ISoftware. getsoft keyboardpossize-Methode (Software BDC. h)
description: Mit der isoftkbd getsoftkeyboardpossize-Methode werden die Anfangsposition und die Größe einer Soft Tastatur abgerufen.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Getsoft keyboardpossize-Methode, Text Dienste-Framework
- Getsoft keyboardpossize-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, getsoft keyboardpossize-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340908"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a><span data-ttu-id="dd46f-106">ISOFT kbd:: getsoft keyboardpossize-Methode</span><span class="sxs-lookup"><span data-stu-id="dd46f-106">ISoftKbd::GetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="dd46f-107">Mit der **isoftkbd:: getsoftkeyboardpossize** -Methode werden die Anfangsposition und die Größe einer Soft Tastatur abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dd46f-107">The **ISoftKbd::GetSoftKeyboardPosSize** method retrieves the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd46f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd46f-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a><span data-ttu-id="dd46f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd46f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd46f-110">*lpstartpoint* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dd46f-110">*lpStartPoint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd46f-111">Ein Zeiger auf einen Puffer, in dem diese Methode eine [Punkt](/previous-versions//dd162805(v=vs.85)) Struktur abruft, die die Koordinaten der oberen linken Position der Soft Tastatur angibt.</span><span class="sxs-lookup"><span data-stu-id="dd46f-111">Pointer to a buffer in which this method retrieves a [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="dd46f-112">*lpwidth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dd46f-112">*lpwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd46f-113">Zeiger auf einen Puffer, in dem diese Methode die Breite der Soft Tastatur abruft.</span><span class="sxs-lookup"><span data-stu-id="dd46f-113">Pointer to a buffer in which this method retrieves the width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="dd46f-114">*lpheight* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dd46f-114">*lpheight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd46f-115">Zeiger auf einen Puffer, in dem diese Methode die Höhe der Soft Tastatur abruft.</span><span class="sxs-lookup"><span data-stu-id="dd46f-115">Pointer to a buffer in which this method retrieves the height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd46f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd46f-116">Return value</span></span>

<span data-ttu-id="dd46f-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd46f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="dd46f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dd46f-118">Value</span></span>                                                                                        | <span data-ttu-id="dd46f-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd46f-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dd46f-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd46f-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dd46f-121">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dd46f-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="dd46f-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dd46f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dd46f-123">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dd46f-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dd46f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd46f-124">Requirements</span></span>



| <span data-ttu-id="dd46f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd46f-125">Requirement</span></span> | <span data-ttu-id="dd46f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dd46f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd46f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd46f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dd46f-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd46f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dd46f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd46f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dd46f-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd46f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dd46f-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dd46f-131">Redistributable</span></span><br/>          | <span data-ttu-id="dd46f-132">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dd46f-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="dd46f-133">Header</span><span class="sxs-lookup"><span data-stu-id="dd46f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd46f-134"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd46f-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="dd46f-135">IDL</span><span class="sxs-lookup"><span data-stu-id="dd46f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd46f-136"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd46f-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="dd46f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dd46f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd46f-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd46f-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd46f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd46f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd46f-140">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="dd46f-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="dd46f-141">**ISOFT kbd:: setsoftware keyboardpossize**</span><span class="sxs-lookup"><span data-stu-id="dd46f-141">**ISoftKbd::SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

