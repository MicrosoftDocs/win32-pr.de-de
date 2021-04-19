---
description: Proxy Funktion für die GetMetadataQueryWriter-Methode.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352675"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="4678c-103">IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="4678c-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="4678c-104">Proxy Funktion für die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4678c-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4678c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4678c-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="4678c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4678c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4678c-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4678c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4678c-108">Typ: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="4678c-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="4678c-109">Zeiger auf dieses [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4678c-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="4678c-110">*ppIMetadataQueryWriter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4678c-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4678c-111">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="4678c-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="4678c-112">Ein Zeiger, der einen Zeiger auf den Metadatenabfragewriter des Encoders empfängt.</span><span class="sxs-lookup"><span data-stu-id="4678c-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4678c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4678c-113">Return value</span></span>

<span data-ttu-id="4678c-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4678c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4678c-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4678c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4678c-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4678c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4678c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4678c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4678c-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4678c-118">Requirements</span></span>



| <span data-ttu-id="4678c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4678c-119">Requirement</span></span> | <span data-ttu-id="4678c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4678c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4678c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4678c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4678c-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4678c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4678c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4678c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4678c-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4678c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4678c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4678c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4678c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4678c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




