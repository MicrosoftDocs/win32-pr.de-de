---
description: Proxy Funktion zum Erstellen von IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348069"
---
# <a name="wiccreateimagingfactory_proxy-function"></a><span data-ttu-id="46e33-103">Wickreateimagingfactory- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="46e33-103">WICCreateImagingFactory\_Proxy function</span></span>

<span data-ttu-id="46e33-104">Proxy Funktion zum Erstellen von [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="46e33-104">Proxy function for creating the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>

## <a name="syntax"></a><span data-ttu-id="46e33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e33-105">Syntax</span></span>

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a><span data-ttu-id="46e33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e33-107">*Sdkversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46e33-107">*SDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e33-108">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="46e33-108">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="46e33-109">*ppiimagingfactory* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="46e33-109">*ppIImagingFactory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e33-110">Typ: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span><span class="sxs-lookup"><span data-stu-id="46e33-110">Type: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e33-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46e33-111">Return value</span></span>

<span data-ttu-id="46e33-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46e33-112">Type: **HRESULT**</span></span>

<span data-ttu-id="46e33-113">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="46e33-113">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46e33-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46e33-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e33-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46e33-115">Remarks</span></span>

<span data-ttu-id="46e33-116">Diese Funktion ist ein Hilfsprogramm zum Erstellen einer WIC-Factory für explizite dll-Verknüpfungen, die für Windows XP erforderlich war.</span><span class="sxs-lookup"><span data-stu-id="46e33-116">This function is a helper for creating a WIC factory for explicit DLL linking, which was needed for Windows XP.</span></span> <span data-ttu-id="46e33-117">Normalerweise würden Sie stattdessen [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) verwenden (siehe [WIC-API-Klassenfactorys](./-wic-api.md#class-factories)), da diese immer in allen neueren Versionen von Windows enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="46e33-117">In normal usage, you would use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instead (see [WIC API class factories](./-wic-api.md#class-factories)), since that's always included in all newer versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e33-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46e33-118">Requirements</span></span>



| <span data-ttu-id="46e33-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46e33-119">Requirement</span></span> | <span data-ttu-id="46e33-120">Wert</span><span class="sxs-lookup"><span data-stu-id="46e33-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e33-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46e33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46e33-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46e33-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="46e33-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46e33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46e33-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46e33-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="46e33-125">DLL</span><span class="sxs-lookup"><span data-stu-id="46e33-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e33-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodebug. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46e33-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt></span></span> </dl> |



 

