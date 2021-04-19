---
description: Schließt die Media Key-Sitzung und muss aufgerufen werden, bevor die schlüsselsitzung freigegeben wird.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'IMF mediakeysession:: Close-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364280"
---
# <a name="imfmediakeysessionclose-method"></a><span data-ttu-id="db788-103">IMF mediakeysession:: Close-Methode</span><span class="sxs-lookup"><span data-stu-id="db788-103">IMFMediaKeySession::Close method</span></span>

<span data-ttu-id="db788-104">Schließt die Media Key-Sitzung und muss aufgerufen werden, bevor die schlüsselsitzung freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="db788-104">Closes the media key session and must be called before the key session is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="db788-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db788-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="db788-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db788-106">Parameters</span></span>

<span data-ttu-id="db788-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="db788-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db788-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db788-108">Return value</span></span>

<span data-ttu-id="db788-109">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="db788-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db788-110">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db788-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db788-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db788-111">Requirements</span></span>



| <span data-ttu-id="db788-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db788-112">Requirement</span></span> | <span data-ttu-id="db788-113">Wert</span><span class="sxs-lookup"><span data-stu-id="db788-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db788-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db788-114">Minimum supported client</span></span><br/> | <span data-ttu-id="db788-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="db788-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="db788-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db788-116">Minimum supported server</span></span><br/> | <span data-ttu-id="db788-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db788-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="db788-118">IDL</span><span class="sxs-lookup"><span data-stu-id="db788-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db788-119"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db788-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db788-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db788-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db788-121">**IMF mediakeysession**</span><span class="sxs-lookup"><span data-stu-id="db788-121">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




