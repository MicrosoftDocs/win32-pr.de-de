---
title: Icdkbd setsoft keyboardpossize-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardpossize-Methode legt die Anfangsposition und die Größe einer Soft Tastatur fest.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Setsoft keyboardpossize-Methode, Text Dienste-Framework
- Setsoft keyboardpossize-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardpossize-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478207"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a><span data-ttu-id="ef233-106">ISOFT kbd:: setsoft keyboardpossize-Methode</span><span class="sxs-lookup"><span data-stu-id="ef233-106">ISoftKbd::SetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="ef233-107">Die **isoftkbd:: setsoftkeyboardpossize** -Methode legt die Anfangsposition und die Größe einer Soft Tastatur fest.</span><span class="sxs-lookup"><span data-stu-id="ef233-107">The **ISoftKbd::SetSoftKeyboardPosSize** method sets the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef233-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef233-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a><span data-ttu-id="ef233-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef233-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef233-110">*Startpunkt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef233-110">*StartPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef233-111">Eine [Punkt](/previous-versions//dd162805(v=vs.85)) Struktur, die die Koordinaten der oberen linken Position der Soft Tastatur angibt.</span><span class="sxs-lookup"><span data-stu-id="ef233-111">A [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="ef233-112">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef233-112">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef233-113">Breite der Bildschirmtastatur.</span><span class="sxs-lookup"><span data-stu-id="ef233-113">Width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="ef233-114">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef233-114">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef233-115">Höhe der Bildschirmtastatur.</span><span class="sxs-lookup"><span data-stu-id="ef233-115">Height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef233-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef233-116">Return value</span></span>

<span data-ttu-id="ef233-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ef233-117">This method can return one of these values.</span></span>



| <span data-ttu-id="ef233-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ef233-118">Value</span></span>                                                                                        | <span data-ttu-id="ef233-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef233-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ef233-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef233-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ef233-121">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ef233-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="ef233-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ef233-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ef233-123">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ef233-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef233-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef233-124">Requirements</span></span>



| <span data-ttu-id="ef233-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef233-125">Requirement</span></span> | <span data-ttu-id="ef233-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ef233-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef233-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef233-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ef233-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef233-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef233-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef233-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ef233-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef233-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ef233-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ef233-131">Redistributable</span></span><br/>          | <span data-ttu-id="ef233-132">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ef233-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ef233-133">Header</span><span class="sxs-lookup"><span data-stu-id="ef233-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef233-134"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef233-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ef233-135">IDL</span><span class="sxs-lookup"><span data-stu-id="ef233-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef233-136"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef233-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef233-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ef233-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef233-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef233-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef233-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef233-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef233-140">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="ef233-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

