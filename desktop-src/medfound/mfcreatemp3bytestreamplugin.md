---
description: Erstellt einen bytestreamhandler für die MP3-Medienquelle.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348233"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a><span data-ttu-id="29d8d-103">MFCreateMP3ByteStreamPlugin-Funktion</span><span class="sxs-lookup"><span data-stu-id="29d8d-103">MFCreateMP3ByteStreamPlugin function</span></span>

<span data-ttu-id="29d8d-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="29d8d-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="29d8d-105">Stattdessen sollten Anwendungen den [quellresolver](source-resolver.md) verwenden, um die MP3-Medienquelle zu erstellen.\]</span><span class="sxs-lookup"><span data-stu-id="29d8d-105">Instead, applications should use the [Source Resolver](source-resolver.md) to create the MP3 media source.\]</span></span>

<span data-ttu-id="29d8d-106">Erstellt einen bytestreamhandler für die MP3-Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="29d8d-106">Creates a byte-stream handler for the MP3 media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d8d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="29d8d-107">Syntax</span></span>


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a><span data-ttu-id="29d8d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29d8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29d8d-109">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29d8d-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29d8d-110">Der Schnittstellenbezeichner (Interface Identifier, IID) der angeforderten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="29d8d-110">The interface identifier (IID) of the requested interface.</span></span> <span data-ttu-id="29d8d-111">Legen Sie diesen Parameter auf **IID \_ imfbytestreamhandler** fest, um einen Zeiger auf die [**imfbytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="29d8d-111">Set this parameter to **IID\_IMFByteStreamHandler** to receive a pointer to the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span>

</dd> <dt>

<span data-ttu-id="29d8d-112">*ppvhandler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="29d8d-112">*ppvHandler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29d8d-113">Empfängt einen Zeiger auf die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="29d8d-113">Receives a pointer to the interface.</span></span> <span data-ttu-id="29d8d-114">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="29d8d-114">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29d8d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29d8d-115">Return value</span></span>

<span data-ttu-id="29d8d-116">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="29d8d-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29d8d-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29d8d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29d8d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29d8d-118">Remarks</span></span>

<span data-ttu-id="29d8d-119">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="29d8d-119">This function has no associated import library.</span></span> <span data-ttu-id="29d8d-120">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit mf.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="29d8d-120">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to mf.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="29d8d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29d8d-121">Requirements</span></span>



| <span data-ttu-id="29d8d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29d8d-122">Requirement</span></span> | <span data-ttu-id="29d8d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="29d8d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="29d8d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29d8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="29d8d-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29d8d-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="29d8d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29d8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="29d8d-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29d8d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="29d8d-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="29d8d-128">End of client support</span></span><br/>    | <span data-ttu-id="29d8d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29d8d-129">Windows Vista</span></span><br/>                             |
| <span data-ttu-id="29d8d-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="29d8d-130">End of server support</span></span><br/>    | <span data-ttu-id="29d8d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29d8d-131">Windows Server 2008</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="29d8d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29d8d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d8d-133">Media Foundation Funktionen</span><span class="sxs-lookup"><span data-stu-id="29d8d-133">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> <dt>

[<span data-ttu-id="29d8d-134">Schema Handler und Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="29d8d-134">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="29d8d-135">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="29d8d-135">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
