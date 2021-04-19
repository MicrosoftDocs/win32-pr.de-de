---
description: Die get \_ Invert-Methode ruft einen booleschen Wert ab, der angibt, ob der Schlüssel Vorgang invertiert wird. Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Idxtkey:: get_Invert-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359316"
---
# <a name="idxtkeyget_invert-method"></a><span data-ttu-id="d969f-104">Idxtkey:: get \_ Invert-Methode</span><span class="sxs-lookup"><span data-stu-id="d969f-104">IDxtKey::get\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="d969f-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d969f-105">\[Deprecated.</span></span> <span data-ttu-id="d969f-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d969f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d969f-107">Die- `get_Invert` Methode ruft einen booleschen Wert ab, der angibt, ob der Schlüssel Vorgang invertiert wird.</span><span class="sxs-lookup"><span data-stu-id="d969f-107">The `get_Invert` method retrieves a Boolean value indicating whether the key operation is inverted.</span></span> <span data-ttu-id="d969f-108">Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="d969f-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="d969f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d969f-109">Syntax</span></span>


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d969f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d969f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d969f-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d969f-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d969f-112">Empfängt einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="d969f-112">Receives one of the following values.</span></span>



| <span data-ttu-id="d969f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d969f-113">Value</span></span>     | <span data-ttu-id="d969f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d969f-114">Description</span></span>                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d969f-115">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="d969f-115">**TRUE**</span></span>  | <span data-ttu-id="d969f-116">Pixel im überlappenden Bild werden in Bezug auf den Standard Vorgang invertiert.</span><span class="sxs-lookup"><span data-stu-id="d969f-116">Pixels in the overlying image are inverted with respect to the default operation.</span></span> |
| <span data-ttu-id="d969f-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d969f-117">**FALSE**</span></span> | <span data-ttu-id="d969f-118">Pixel im überliegenden Bild werden standardmäßig transparent gemacht.</span><span class="sxs-lookup"><span data-stu-id="d969f-118">Pixels in the overlying image are made transparent in the default manner.</span></span>         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d969f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d969f-119">Return value</span></span>

<span data-ttu-id="d969f-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d969f-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d969f-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d969f-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d969f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d969f-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d969f-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d969f-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d969f-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d969f-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d969f-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d969f-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d969f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d969f-126">Requirements</span></span>



| <span data-ttu-id="d969f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d969f-127">Requirement</span></span> | <span data-ttu-id="d969f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d969f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d969f-129">Header</span><span class="sxs-lookup"><span data-stu-id="d969f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d969f-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d969f-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d969f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d969f-131">Library</span></span><br/> | <dl> <span data-ttu-id="d969f-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d969f-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d969f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d969f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d969f-134">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d969f-134">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="d969f-135">**Idxtkey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="d969f-135">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




