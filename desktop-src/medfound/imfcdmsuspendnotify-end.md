---
description: Der tatsächliche Anhaltevorgang wird durchgeführt, und es werden keine weiteren Aufrufe in das Modul zur Inhalts Entschlüsselung (CDM) durchgeführt.
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'IMF cdmsuspendnotify:: End-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362414"
---
# <a name="imfcdmsuspendnotifyend-method"></a><span data-ttu-id="471d4-103">IMF cdmsuspendnotify:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="471d4-103">IMFCdmSuspendNotify::End method</span></span>

<span data-ttu-id="471d4-104">Der tatsächliche Anhaltevorgang wird durchgeführt, und es werden keine weiteren Aufrufe in das Modul zur Inhalts Entschlüsselung (CDM) durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="471d4-104">The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="471d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="471d4-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="471d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="471d4-106">Parameters</span></span>

<span data-ttu-id="471d4-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="471d4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="471d4-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="471d4-108">Return value</span></span>

<span data-ttu-id="471d4-109">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="471d4-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="471d4-110">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="471d4-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="471d4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="471d4-111">Requirements</span></span>



| <span data-ttu-id="471d4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="471d4-112">Requirement</span></span> | <span data-ttu-id="471d4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="471d4-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="471d4-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="471d4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="471d4-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="471d4-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="471d4-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="471d4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="471d4-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="471d4-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="471d4-118">IDL</span><span class="sxs-lookup"><span data-stu-id="471d4-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="471d4-119"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="471d4-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="471d4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="471d4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471d4-121">**IMF cdmsuspendnotify**</span><span class="sxs-lookup"><span data-stu-id="471d4-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




