---
title: ISOFT kbd showkeysforkeyscanmode-Methode ("Soft kbdc. h")
description: Die isoftkbd showkeysforkeyscanmode-Methode zeigt die Schlüssel an, die für den Schlüssel Scan Modus für eine weiche Tastatur verwendet werden.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Showkeysforkeyscanmode-Methode, Text Dienste-Framework
- Showkeysforkeyscanmode-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, showkeysforkeyscanmode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478204"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a><span data-ttu-id="b32db-106">ISOFT kbd:: showkeysforkeyscanmode-Methode</span><span class="sxs-lookup"><span data-stu-id="b32db-106">ISoftKbd::ShowKeysForKeyScanMode method</span></span>

<span data-ttu-id="b32db-107">Die **isoftkbd:: showkeysforkeyscanmode** -Methode zeigt die Schlüssel an, die für den Schlüssel Scan Modus für eine weiche Tastatur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b32db-107">The **ISoftKbd::ShowKeysForKeyScanMode** method displays the keys used for the key scan mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32db-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b32db-108">Syntax</span></span>


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a><span data-ttu-id="b32db-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b32db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32db-110">*lpkeyid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b32db-110">*lpKeyID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b32db-111">Ein Zeiger auf ein Array von keyid-Elementen, die die Bezeichner von Schlüsseln angeben, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b32db-111">Pointer to an array of KEYID elements indicating the identifiers of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="b32db-112">*ikeynum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b32db-112">*iKeyNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b32db-113">Die Anzahl der anzuzeigenden Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b32db-113">The number of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="b32db-114">vollständig  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b32db-114">*fHighL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b32db-115">TRUE, wenn die-Methode die Schlüssel hervorheben soll, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b32db-115">TRUE if the method is to highlight the keys, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b32db-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b32db-116">Return value</span></span>

<span data-ttu-id="b32db-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b32db-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b32db-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b32db-118">Value</span></span>                                                                                        | <span data-ttu-id="b32db-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b32db-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b32db-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b32db-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b32db-121">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b32db-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="b32db-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b32db-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b32db-123">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b32db-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b32db-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b32db-124">Requirements</span></span>



| <span data-ttu-id="b32db-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b32db-125">Requirement</span></span> | <span data-ttu-id="b32db-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b32db-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b32db-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b32db-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b32db-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b32db-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b32db-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b32db-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b32db-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b32db-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b32db-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b32db-131">Redistributable</span></span><br/>          | <span data-ttu-id="b32db-132">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b32db-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="b32db-133">Header</span><span class="sxs-lookup"><span data-stu-id="b32db-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b32db-134"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="b32db-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="b32db-135">IDL</span><span class="sxs-lookup"><span data-stu-id="b32db-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b32db-136"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b32db-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="b32db-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b32db-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b32db-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b32db-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b32db-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b32db-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32db-140">**Iweichkbd**</span><span class="sxs-lookup"><span data-stu-id="b32db-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





