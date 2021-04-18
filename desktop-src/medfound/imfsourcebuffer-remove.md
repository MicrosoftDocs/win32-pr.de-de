---
description: Entfernt die Medien Segmente, die durch den angegebenen Zeitbereich definiert sind, aus IMF sourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'IMF sourceBuffer:: Remove-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: d82660d08efe651b321672b6ccd0cb475875beee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345799"
---
# <a name="imfsourcebufferremove-method"></a><span data-ttu-id="13a2a-103">IMF sourceBuffer:: Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="13a2a-103">IMFSourceBuffer::Remove method</span></span>

<span data-ttu-id="13a2a-104">Entfernt die Medien Segmente, die durch den angegebenen Zeitbereich definiert sind, aus [**IMF sourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="13a2a-104">Removes the media segments defined by the specified time range from the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="13a2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13a2a-105">Syntax</span></span>


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a><span data-ttu-id="13a2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13a2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a2a-107">*starten* \[ Sie in\]</span><span class="sxs-lookup"><span data-stu-id="13a2a-107">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a2a-108">Der Anfang des Zeit Bereichs.</span><span class="sxs-lookup"><span data-stu-id="13a2a-108">The start of the time range.</span></span>

</dd> <dt>

<span data-ttu-id="13a2a-109">*Ende* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13a2a-109">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a2a-110">Das Ende des Zeit Bereichs.</span><span class="sxs-lookup"><span data-stu-id="13a2a-110">The end of the time range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a2a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13a2a-111">Return value</span></span>

<span data-ttu-id="13a2a-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="13a2a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13a2a-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13a2a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a2a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13a2a-114">Requirements</span></span>



| <span data-ttu-id="13a2a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13a2a-115">Requirement</span></span> | <span data-ttu-id="13a2a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="13a2a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a2a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13a2a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="13a2a-118">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="13a2a-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="13a2a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13a2a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="13a2a-120">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13a2a-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="13a2a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="13a2a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13a2a-122"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13a2a-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a2a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13a2a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a2a-124">**IMF sourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="13a2a-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




