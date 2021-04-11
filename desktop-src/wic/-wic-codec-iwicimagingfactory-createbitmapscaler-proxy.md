---
description: Proxy Funktion für die Methode "kreatebitmapscaler".
ms.assetid: 27fcb17e-bdcd-44cc-9fe6-f93816589b50
title: IWICImagingFactory_CreateBitmapScaler_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapScaler_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ac831427901de481d313833e4ca8459ccd333384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960495"
---
# <a name="iwicimagingfactory_createbitmapscaler_proxy-function"></a><span data-ttu-id="efc84-103">IWICImagingFactory- \_ Funktion "foratebitmapscaler \_ Proxy"</span><span class="sxs-lookup"><span data-stu-id="efc84-103">IWICImagingFactory\_CreateBitmapScaler\_Proxy function</span></span>

<span data-ttu-id="efc84-104">Proxy Funktion für die Methode " [**kreatebitmapscaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) ".</span><span class="sxs-lookup"><span data-stu-id="efc84-104">Proxy function for the [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="efc84-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapScaler_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapScaler   **ppIBitmapScaler
);
```



## <a name="parameters"></a><span data-ttu-id="efc84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="efc84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc84-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efc84-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc84-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="efc84-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="efc84-109">_ppIBitmapScaler \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efc84-109">_ppIBitmapScaler\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efc84-110">Typ: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span><span class="sxs-lookup"><span data-stu-id="efc84-110">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span></span>

<span data-ttu-id="efc84-111">Ein Zeiger, der einen Zeiger auf ein neues [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)-Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="efc84-111">A pointer that receives a pointer to a new [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc84-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efc84-112">Return value</span></span>

<span data-ttu-id="efc84-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="efc84-113">Type: **HRESULT**</span></span>

<span data-ttu-id="efc84-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="efc84-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="efc84-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="efc84-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="efc84-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efc84-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="efc84-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="efc84-117">Requirements</span></span>



| <span data-ttu-id="efc84-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efc84-118">Requirement</span></span> | <span data-ttu-id="efc84-119">Wert</span><span class="sxs-lookup"><span data-stu-id="efc84-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efc84-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efc84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="efc84-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efc84-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="efc84-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efc84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="efc84-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efc84-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="efc84-124">DLL</span><span class="sxs-lookup"><span data-stu-id="efc84-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efc84-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efc84-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




