---
title: ISOFT kbd enumsoft Keyboard-Methode (Software-Domänen Controller. h)
description: Die isoftkbd enumsoftkeyboard-Methode listet die möglichen weichen Tastaturen auf, die die angegebene Sprache unterstützen.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Enumsoft Keyboard-Methode, Text Dienste-Framework
- Enumsoft Keyboard-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, enumsoft Keyboard-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478000"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a><span data-ttu-id="ace0b-106">Iweichkbd:: enumsoft Keyboard-Methode</span><span class="sxs-lookup"><span data-stu-id="ace0b-106">ISoftKbd::EnumSoftKeyboard method</span></span>

<span data-ttu-id="ace0b-107">Die **isoftkbd:: enumsoftkeyboard** -Methode listet die möglichen weichen Tastaturen auf, die die angegebene Sprache unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ace0b-107">The **ISoftKbd::EnumSoftKeyboard** method enumerates the possible soft keyboards that support the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace0b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ace0b-108">Syntax</span></span>


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a><span data-ttu-id="ace0b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ace0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace0b-110">*LangID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace0b-110">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace0b-111">Der Sprachen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ace0b-111">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ace0b-112">*lpdwkeyboard* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ace0b-112">*lpdwKeyboard* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ace0b-113">Zeiger auf einen Puffer, in dem diese Methode Bezeichner der verfügbaren Soft Tastaturen abruft.</span><span class="sxs-lookup"><span data-stu-id="ace0b-113">Pointer to a buffer in which this method retrieves identifiers of the available soft keyboards.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace0b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ace0b-114">Return value</span></span>

<span data-ttu-id="ace0b-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ace0b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ace0b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ace0b-116">Value</span></span>                                                                                        | <span data-ttu-id="ace0b-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ace0b-117">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="ace0b-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ace0b-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ace0b-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ace0b-119">The method was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="ace0b-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ace0b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ace0b-121">Der *LangID* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ace0b-121">The *langid* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ace0b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ace0b-122">Requirements</span></span>



| <span data-ttu-id="ace0b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ace0b-123">Requirement</span></span> | <span data-ttu-id="ace0b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ace0b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ace0b-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ace0b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ace0b-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ace0b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ace0b-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ace0b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ace0b-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ace0b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ace0b-129">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ace0b-129">Redistributable</span></span><br/>          | <span data-ttu-id="ace0b-130">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ace0b-130">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ace0b-131">Header</span><span class="sxs-lookup"><span data-stu-id="ace0b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace0b-132"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace0b-132"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ace0b-133">IDL</span><span class="sxs-lookup"><span data-stu-id="ace0b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ace0b-134"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ace0b-134"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ace0b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ace0b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace0b-136"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace0b-136"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace0b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ace0b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace0b-138">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="ace0b-138">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





