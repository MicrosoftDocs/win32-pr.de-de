---
description: Gibt eine Zeichenfolge zurück, die die Plug & Play-ID für das Tablet-Gerät enthält.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'ITablet:: getplugandplayid-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349490"
---
# <a name="itabletgetplugandplayid-method"></a><span data-ttu-id="abc77-103">ITablet:: getplugandplayid-Methode</span><span class="sxs-lookup"><span data-stu-id="abc77-103">ITablet::GetPlugAndPlayId method</span></span>

<span data-ttu-id="abc77-104">Gibt eine Zeichenfolge zurück, die die Plug & Play-ID für das Tablet-Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="abc77-104">Returns a string containing the Plug and Play ID for the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abc77-105">Syntax</span></span>


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a><span data-ttu-id="abc77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abc77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc77-107">*ppwszppid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="abc77-107">*ppwszPPId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abc77-108">Zeiger auf eine Zeichenfolge, die die Plug & Play ID für das Tablet-Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="abc77-108">Pointer to a string containing the Plug and Play ID for the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc77-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abc77-109">Return value</span></span>

<span data-ttu-id="abc77-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="abc77-110">This method can return one of these values.</span></span>



| <span data-ttu-id="abc77-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="abc77-111">Return code</span></span>                                                                            | <span data-ttu-id="abc77-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abc77-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="abc77-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abc77-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="abc77-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="abc77-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="abc77-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="abc77-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="abc77-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="abc77-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abc77-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abc77-117">Remarks</span></span>

<span data-ttu-id="abc77-118">Es ist Aufgabe des Aufrufers, den von dieser Methode zurückgegebenen Speicher mithilfe von " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)" freizugeben.</span><span class="sxs-lookup"><span data-stu-id="abc77-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="abc77-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abc77-119">Requirements</span></span>



| <span data-ttu-id="abc77-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abc77-120">Requirement</span></span> | <span data-ttu-id="abc77-121">Wert</span><span class="sxs-lookup"><span data-stu-id="abc77-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abc77-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abc77-122">Minimum supported client</span></span><br/> | <span data-ttu-id="abc77-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abc77-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="abc77-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abc77-124">Minimum supported server</span></span><br/> | <span data-ttu-id="abc77-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="abc77-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="abc77-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="abc77-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="abc77-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abc77-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abc77-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abc77-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc77-129">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="abc77-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

