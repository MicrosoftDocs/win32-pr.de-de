---
description: Fügt der Auflistung der Puffer, die der imfmediasourceextension zugeordnet sind, einen imfsourcebuffer hinzu.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'Imfmediasourceextension:: addsourcebuffer-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355713"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a><span data-ttu-id="a8f49-103">Imfmediasourceextension:: addsourcebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="a8f49-103">IMFMediaSourceExtension::AddSourceBuffer method</span></span>

<span data-ttu-id="a8f49-104">Fügt der Auflistung der Puffer, die der [**imfmediasourceextension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)zugeordnet sind, einen [**imfsourcebuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8f49-104">Adds a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) to the collection of buffers associated with the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8f49-105">Syntax</span></span>


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a8f49-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f49-107">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8f49-107">*type* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a8f49-108">*pnotify* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8f49-108">*pNotify* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a8f49-109">*ppsourcebuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a8f49-109">*ppSourceBuffer* \[out\]</span></span>
<span data-ttu-id="a8f49-110"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a8f49-110"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="a8f49-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8f49-111">Return value</span></span>

<span data-ttu-id="a8f49-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a8f49-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8f49-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8f49-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f49-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8f49-114">Requirements</span></span>



| <span data-ttu-id="a8f49-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8f49-115">Requirement</span></span> | <span data-ttu-id="a8f49-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a8f49-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f49-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8f49-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f49-118">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a8f49-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a8f49-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8f49-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f49-120">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8f49-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a8f49-121">IDL</span><span class="sxs-lookup"><span data-stu-id="a8f49-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8f49-122"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8f49-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f49-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8f49-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f49-124">**Imfmediasourceextension**</span><span class="sxs-lookup"><span data-stu-id="a8f49-124">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




