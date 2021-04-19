---
description: Die get \_ Alpha-Methode ruft den Alpha-Wert für das gesamte Bild ab.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Idxtalphasetter:: get_Alpha-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367013"
---
# <a name="idxtalphasetterget_alpha-method"></a><span data-ttu-id="bf7db-103">Idxtalphasetter:: get \_ Alpha-Methode</span><span class="sxs-lookup"><span data-stu-id="bf7db-103">IDxtAlphaSetter::get\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="bf7db-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="bf7db-104">\[Deprecated.</span></span> <span data-ttu-id="bf7db-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="bf7db-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bf7db-106">Die- `get_Alpha` Methode ruft den Alpha-Wert für das gesamte Bild ab.</span><span class="sxs-lookup"><span data-stu-id="bf7db-106">The `get_Alpha` method retrieves the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf7db-107">Syntax</span></span>


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="bf7db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf7db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7db-109">*Palpha* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bf7db-109">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7db-110">Empfängt den Alpha-Wert.</span><span class="sxs-lookup"><span data-stu-id="bf7db-110">Receives the alpha value.</span></span> <span data-ttu-id="bf7db-111">Dieser Alpha Wert wird auf das gesamte Zielbild angewendet.</span><span class="sxs-lookup"><span data-stu-id="bf7db-111">This alpha value will be applied to the entire target image.</span></span> <span data-ttu-id="bf7db-112">Ein negativer Wert gibt an, dass kein Alpha Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bf7db-112">A negative value indicates that no alpha value is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf7db-113">Return value</span></span>

<span data-ttu-id="bf7db-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bf7db-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bf7db-115">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="bf7db-115">Possible values include the following.</span></span>



| <span data-ttu-id="bf7db-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bf7db-116">Return code</span></span>                                                                               | <span data-ttu-id="bf7db-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf7db-117">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="bf7db-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7db-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="bf7db-119">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="bf7db-119">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="bf7db-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7db-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="bf7db-121">Erfolg</span><span class="sxs-lookup"><span data-stu-id="bf7db-121">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="bf7db-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf7db-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf7db-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="bf7db-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bf7db-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="bf7db-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bf7db-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf7db-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf7db-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf7db-126">Requirements</span></span>



| <span data-ttu-id="bf7db-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf7db-127">Requirement</span></span> | <span data-ttu-id="bf7db-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7db-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7db-129">Header</span><span class="sxs-lookup"><span data-stu-id="bf7db-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bf7db-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="bf7db-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bf7db-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bf7db-131">Library</span></span><br/> | <dl> <span data-ttu-id="bf7db-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="bf7db-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7db-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf7db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7db-134">**Idxtalphasetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bf7db-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




