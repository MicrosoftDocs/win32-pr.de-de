---
description: Fügt das angegebene mediensegment an imfsourcebuffer an.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: 'IMF sourceBuffer:: Append-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214890"
---
# <a name="imfsourcebufferappend-method"></a><span data-ttu-id="95b2a-103">IMF sourceBuffer:: Append-Methode</span><span class="sxs-lookup"><span data-stu-id="95b2a-103">IMFSourceBuffer::Append method</span></span>

<span data-ttu-id="95b2a-104">Fügt das angegebene mediensegment an [**imfsourcebuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)an.</span><span class="sxs-lookup"><span data-stu-id="95b2a-104">Appends the specified media segment to the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="95b2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b2a-105">Syntax</span></span>


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a><span data-ttu-id="95b2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95b2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b2a-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b2a-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b2a-108">Die anzufügende Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="95b2a-108">The media data to append.</span></span>

</dd> <dt>

<span data-ttu-id="95b2a-109">*len* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b2a-109">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b2a-110">Die Länge der in *pData* gespeicherten Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="95b2a-110">The length of the media data stored in *pData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b2a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95b2a-111">Return value</span></span>

<span data-ttu-id="95b2a-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="95b2a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95b2a-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95b2a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b2a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95b2a-114">Requirements</span></span>



| <span data-ttu-id="95b2a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95b2a-115">Requirement</span></span> | <span data-ttu-id="95b2a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="95b2a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b2a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95b2a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="95b2a-118">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="95b2a-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="95b2a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95b2a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="95b2a-120">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95b2a-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="95b2a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="95b2a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95b2a-122"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95b2a-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b2a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b2a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b2a-124">**IMF sourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="95b2a-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




