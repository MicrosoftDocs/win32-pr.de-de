---
description: Entfernt den angegebenen Quell Puffer aus der Auflistung der Quell Puffer, die vom imfmediasourceextension-Objekt verwaltet werden.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'Imfmediasourceextension:: removesourcebuffer-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351518"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a><span data-ttu-id="64f0e-103">Imfmediasourceextension:: removesourcebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="64f0e-103">IMFMediaSourceExtension::RemoveSourceBuffer method</span></span>

<span data-ttu-id="64f0e-104">Entfernt den angegebenen Quell Puffer aus der Auflistung der Quell Puffer, die vom [**imfmediasourceextension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) -Objekt verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="64f0e-104">Removes the specified source buffer from the collection of source buffers managed by the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f0e-105">Syntax</span></span>


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="64f0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f0e-107">*psourcebuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f0e-107">*pSourceBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f0e-108">Der Puffer, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64f0e-108">The buffer to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f0e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f0e-109">Return value</span></span>

<span data-ttu-id="64f0e-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="64f0e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64f0e-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64f0e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f0e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f0e-112">Requirements</span></span>



| <span data-ttu-id="64f0e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f0e-113">Requirement</span></span> | <span data-ttu-id="64f0e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="64f0e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f0e-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64f0e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="64f0e-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="64f0e-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="64f0e-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64f0e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="64f0e-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64f0e-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="64f0e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="64f0e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64f0e-120"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64f0e-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f0e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f0e-122">**Imfmediasourceextension**</span><span class="sxs-lookup"><span data-stu-id="64f0e-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




