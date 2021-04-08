---
title: ISOFT kbd ShowSoft Keyboard-Methode (Software-DC. h)
description: Die isoftkbd showsoftkeyboard-Methode zeigt eine weiche Tastatur an.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- ShowSoft Keyboard-Methode, Text Dienste-Framework
- ShowSoft Keyboard-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, ShowSoft Keyboard-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040062"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a><span data-ttu-id="1c1db-106">ISOFT kbd:: ShowSoft Keyboard-Methode</span><span class="sxs-lookup"><span data-stu-id="1c1db-106">ISoftKbd::ShowSoftKeyboard method</span></span>

<span data-ttu-id="1c1db-107">Die **isoftkbd:: showsoftkeyboard** -Methode zeigt eine weiche Tastatur an.</span><span class="sxs-lookup"><span data-stu-id="1c1db-107">The **ISoftKbd::ShowSoftKeyboard** method displays a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1db-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c1db-108">Syntax</span></span>


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a><span data-ttu-id="1c1db-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c1db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1db-110">*IShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c1db-110">*iShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1db-111">Eine ganze Zahl, die den Typ der anzuzeigenden Bildschirmtastatur angibt.</span><span class="sxs-lookup"><span data-stu-id="1c1db-111">Integer indicating the type of soft keyboard to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1db-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c1db-112">Return value</span></span>

<span data-ttu-id="1c1db-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1c1db-113">This method can return one of these values.</span></span>



| <span data-ttu-id="1c1db-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1c1db-114">Value</span></span>                                                                                | <span data-ttu-id="1c1db-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c1db-115">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1c1db-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1db-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1c1db-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1c1db-117">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c1db-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c1db-118">Requirements</span></span>



| <span data-ttu-id="1c1db-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c1db-119">Requirement</span></span> | <span data-ttu-id="1c1db-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1c1db-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1db-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c1db-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1db-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c1db-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1c1db-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c1db-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1db-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c1db-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1c1db-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1c1db-125">Redistributable</span></span><br/>          | <span data-ttu-id="1c1db-126">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1c1db-126">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1c1db-127">Header</span><span class="sxs-lookup"><span data-stu-id="1c1db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c1db-128"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1db-128"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1c1db-129">IDL</span><span class="sxs-lookup"><span data-stu-id="1c1db-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c1db-130"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c1db-130"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="1c1db-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1c1db-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c1db-132"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c1db-132"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1db-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c1db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1db-134">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="1c1db-134">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





