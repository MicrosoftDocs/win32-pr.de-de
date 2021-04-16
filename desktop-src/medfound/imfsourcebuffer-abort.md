---
description: Bricht die Verarbeitung des aktuellen Medien Segments ab.
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: 'IMF sourceBuffer:: Abort-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 3a8b5115032fb918af66094bb87c7118eb503da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527680"
---
# <a name="imfsourcebufferabort-method"></a><span data-ttu-id="a5fb6-103">IMF sourceBuffer:: Abort-Methode</span><span class="sxs-lookup"><span data-stu-id="a5fb6-103">IMFSourceBuffer::Abort method</span></span>

<span data-ttu-id="a5fb6-104">Bricht die Verarbeitung des aktuellen Medien Segments ab.</span><span class="sxs-lookup"><span data-stu-id="a5fb6-104">Aborts the processing of the current media segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fb6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5fb6-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="a5fb6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5fb6-106">Parameters</span></span>

<span data-ttu-id="a5fb6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a5fb6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5fb6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5fb6-108">Return value</span></span>

<span data-ttu-id="a5fb6-109">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a5fb6-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5fb6-110">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5fb6-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fb6-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5fb6-111">Requirements</span></span>



| <span data-ttu-id="a5fb6-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5fb6-112">Requirement</span></span> | <span data-ttu-id="a5fb6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a5fb6-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fb6-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5fb6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a5fb6-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a5fb6-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a5fb6-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5fb6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a5fb6-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5fb6-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a5fb6-118">IDL</span><span class="sxs-lookup"><span data-stu-id="a5fb6-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5fb6-119"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5fb6-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5fb6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5fb6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fb6-121">**IMF sourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="a5fb6-121">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




