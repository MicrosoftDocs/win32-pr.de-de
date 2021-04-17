---
title: ISoftware Type getsoft keyboardtypemode-Methode (Software-DC. h)
description: Die isoftkbd getsoftkeyboardtypemode-Methode ruft den typmodus für eine weiche Tastatur ab.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Getsoft keyboardtypemode-Methode, Text Dienste-Framework
- Getsoft keyboardtypemode-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, getsoft keyboardtypemode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391495"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a><span data-ttu-id="12fa4-106">ISOFT kbd:: getsoft keyboardtypemode-Methode</span><span class="sxs-lookup"><span data-stu-id="12fa4-106">ISoftKbd::GetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="12fa4-107">Die **isoftkbd:: getsoftkeyboardtypemode** -Methode ruft den typmodus für eine weiche Tastatur ab.</span><span class="sxs-lookup"><span data-stu-id="12fa4-107">The **ISoftKbd::GetSoftKeyboardTypeMode** method retrieves the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fa4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="12fa4-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="12fa4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="12fa4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fa4-110">*lptypemode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12fa4-110">*lpTypeMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa4-111">Zeiger auf einen Puffer, in dem diese Methode den typmodus abruft.</span><span class="sxs-lookup"><span data-stu-id="12fa4-111">Pointer to a buffer in which this method retrieves the type mode.</span></span> <span data-ttu-id="12fa4-112">Mögliche Werte sind für die [**typemode**](typemode.md) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="12fa4-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fa4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12fa4-113">Return value</span></span>

<span data-ttu-id="12fa4-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="12fa4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="12fa4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="12fa4-115">Value</span></span>                                                                                        | <span data-ttu-id="12fa4-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12fa4-116">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="12fa4-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12fa4-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="12fa4-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="12fa4-118">The method was successful.</span></span><br/>             |
| <dl> <span data-ttu-id="12fa4-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="12fa4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="12fa4-120">Der *lptypemode* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="12fa4-120">The *lpTypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="12fa4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12fa4-121">Requirements</span></span>



| <span data-ttu-id="12fa4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12fa4-122">Requirement</span></span> | <span data-ttu-id="12fa4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="12fa4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12fa4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12fa4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12fa4-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12fa4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12fa4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12fa4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12fa4-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12fa4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="12fa4-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="12fa4-128">Redistributable</span></span><br/>          | <span data-ttu-id="12fa4-129">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="12fa4-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="12fa4-130">Header</span><span class="sxs-lookup"><span data-stu-id="12fa4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="12fa4-131"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fa4-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="12fa4-132">IDL</span><span class="sxs-lookup"><span data-stu-id="12fa4-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12fa4-133"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12fa4-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="12fa4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="12fa4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12fa4-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12fa4-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12fa4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12fa4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fa4-137">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="12fa4-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="12fa4-138">**Icdkbd:: setsoft keyboardtypemode**</span><span class="sxs-lookup"><span data-stu-id="12fa4-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="12fa4-139">**Typemode**</span><span class="sxs-lookup"><span data-stu-id="12fa4-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





