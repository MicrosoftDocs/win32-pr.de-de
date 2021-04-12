---
title: Icdkbd setsoft keyboardtypemode-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardtypemode-Methode legt den typmodus für eine weiche Tastatur fest.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Setsoft keyboardtypemode-Methode, Text Dienste-Framework
- Setsoft keyboardtypemode-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardtypemode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478210"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a><span data-ttu-id="5d391-106">ISOFT kbd:: setsoft keyboardtypemode-Methode</span><span class="sxs-lookup"><span data-stu-id="5d391-106">ISoftKbd::SetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="5d391-107">Die **isoftkbd:: setsoftkeyboardtypemode** -Methode legt den typmodus für eine weiche Tastatur fest.</span><span class="sxs-lookup"><span data-stu-id="5d391-107">The **ISoftKbd::SetSoftKeyboardTypeMode** method sets the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d391-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d391-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="5d391-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d391-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d391-110">*Typemode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d391-110">*TypeMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d391-111">Der typmodus.</span><span class="sxs-lookup"><span data-stu-id="5d391-111">The type mode.</span></span> <span data-ttu-id="5d391-112">Mögliche Werte sind für die [**typemode**](typemode.md) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="5d391-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d391-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d391-113">Return value</span></span>

<span data-ttu-id="5d391-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5d391-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5d391-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5d391-115">Value</span></span>                                                                                        | <span data-ttu-id="5d391-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d391-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="5d391-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5d391-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5d391-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5d391-118">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="5d391-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="5d391-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5d391-120">Der *typemode* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5d391-120">The *TypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d391-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d391-121">Requirements</span></span>



| <span data-ttu-id="5d391-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d391-122">Requirement</span></span> | <span data-ttu-id="5d391-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5d391-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d391-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d391-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d391-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d391-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d391-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d391-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d391-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d391-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5d391-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5d391-128">Redistributable</span></span><br/>          | <span data-ttu-id="5d391-129">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d391-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="5d391-130">Header</span><span class="sxs-lookup"><span data-stu-id="5d391-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d391-131"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d391-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="5d391-132">IDL</span><span class="sxs-lookup"><span data-stu-id="5d391-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d391-133"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d391-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="5d391-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5d391-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d391-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d391-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d391-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d391-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d391-137">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="5d391-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="5d391-138">**Iweichkbd:: getsoftware keyboardtypemode**</span><span class="sxs-lookup"><span data-stu-id="5d391-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="5d391-139">**Typemode**</span><span class="sxs-lookup"><span data-stu-id="5d391-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





