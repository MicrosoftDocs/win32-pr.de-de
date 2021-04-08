---
description: Proxy Funktion für die getcolorcount-Methode.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: IWICPalette_GetColorCount_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9518878dd05c6b89152b91863c8996f96b8e6e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866767"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a><span data-ttu-id="5896b-103">Iwicpalette \_ getcolorcount- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="5896b-103">IWICPalette\_GetColorCount\_Proxy function</span></span>

<span data-ttu-id="5896b-104">Proxy Funktion für die [**getcolorcount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5896b-104">Proxy function for the [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5896b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5896b-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="5896b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5896b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5896b-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5896b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5896b-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="5896b-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="5896b-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5896b-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="5896b-110">*pcCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5896b-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5896b-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="5896b-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="5896b-112">Ein Zeiger, der die Anzahl der Farben in der Farbtabelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="5896b-112">Pointer that receives the number of colors in the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5896b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5896b-113">Return value</span></span>

<span data-ttu-id="5896b-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5896b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5896b-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5896b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5896b-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5896b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5896b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5896b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5896b-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5896b-118">Requirements</span></span>



| <span data-ttu-id="5896b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5896b-119">Requirement</span></span> | <span data-ttu-id="5896b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5896b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5896b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5896b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5896b-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5896b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5896b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5896b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5896b-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5896b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5896b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5896b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5896b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5896b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




