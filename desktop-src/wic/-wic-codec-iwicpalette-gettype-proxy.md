---
description: Proxy Funktion für die GetType-Methode.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: IWICPalette_GetType_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363596"
---
# <a name="iwicpalette_gettype_proxy-function"></a><span data-ttu-id="8ad99-103">Iwicpalette \_ GetType- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="8ad99-103">IWICPalette\_GetType\_Proxy function</span></span>

<span data-ttu-id="8ad99-104">Proxy Funktion für die [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8ad99-104">Proxy function for the [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad99-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a><span data-ttu-id="8ad99-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ad99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ad99-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ad99-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad99-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="8ad99-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="8ad99-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8ad99-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="8ad99-110">*etpalettetype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ad99-110">*pePaletteType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad99-111">Typ: \**[**wicbitmappalettetype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _</span><span class="sxs-lookup"><span data-stu-id="8ad99-111">Type: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\** _</span></span>

<span data-ttu-id="8ad99-112">Ein Zeiger, der den Palettentyp von bimtap empfängt.</span><span class="sxs-lookup"><span data-stu-id="8ad99-112">Pointer that receives the palette type of the bimtap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ad99-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ad99-113">Return value</span></span>

<span data-ttu-id="8ad99-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8ad99-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8ad99-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad99-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ad99-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ad99-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ad99-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ad99-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8ad99-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8ad99-118">Requirements</span></span>



| <span data-ttu-id="8ad99-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ad99-119">Requirement</span></span> | <span data-ttu-id="8ad99-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8ad99-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad99-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ad99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8ad99-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ad99-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8ad99-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ad99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8ad99-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ad99-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8ad99-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8ad99-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ad99-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ad99-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




