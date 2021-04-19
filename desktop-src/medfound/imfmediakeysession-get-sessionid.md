---
description: Ruft eine eindeutige Sitzungs-ID ab, die für diese Sitzung erstellt wurde.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'IMF mediakeysession:: get_SessionId-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106369929"
---
# <a name="imfmediakeysessionget_sessionid-method"></a><span data-ttu-id="38018-103">IMF mediakeysession:: get \_ SessionID-Methode</span><span class="sxs-lookup"><span data-stu-id="38018-103">IMFMediaKeySession::get\_SessionId method</span></span>

<span data-ttu-id="38018-104">Ruft eine eindeutige Sitzungs-ID ab, die für diese Sitzung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="38018-104">Gets a unique session id created for this session.</span></span>

## <a name="syntax"></a><span data-ttu-id="38018-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38018-105">Syntax</span></span>


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a><span data-ttu-id="38018-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38018-107">*sessionId*</span><span class="sxs-lookup"><span data-stu-id="38018-107">*sessionId*</span></span> 
</dt> <dd>

<span data-ttu-id="38018-108">Die ID der Medien schlüsselsitzung.</span><span class="sxs-lookup"><span data-stu-id="38018-108">The media key session id.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38018-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38018-109">Return value</span></span>

<span data-ttu-id="38018-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="38018-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38018-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38018-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="38018-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38018-112">Requirements</span></span>



| <span data-ttu-id="38018-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38018-113">Requirement</span></span> | <span data-ttu-id="38018-114">Wert</span><span class="sxs-lookup"><span data-stu-id="38018-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="38018-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38018-115">Minimum supported client</span></span><br/> | <span data-ttu-id="38018-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="38018-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="38018-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38018-117">Minimum supported server</span></span><br/> | <span data-ttu-id="38018-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38018-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="38018-119">IDL</span><span class="sxs-lookup"><span data-stu-id="38018-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38018-120"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38018-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38018-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38018-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38018-122">**IMF mediakeysession**</span><span class="sxs-lookup"><span data-stu-id="38018-122">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




