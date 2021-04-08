---
description: Gibt an, dass der Unterbrechungs Prozess gestartet wird und die Ressourcen in einen konsistenten Zustand versetzt werden sollen.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: 'IMF cdmsuspendnotify:: Begin-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749664"
---
# <a name="imfcdmsuspendnotifybegin-method"></a><span data-ttu-id="48930-103">IMF cdmsuspendnotify:: Begin-Methode</span><span class="sxs-lookup"><span data-stu-id="48930-103">IMFCdmSuspendNotify::Begin method</span></span>

<span data-ttu-id="48930-104">Gibt an, dass der Unterbrechungs Prozess gestartet wird und die Ressourcen in einen konsistenten Zustand versetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="48930-104">Indicates that the suspend process is starting and resources should be brought into a consistent state.</span></span>

## <a name="syntax"></a><span data-ttu-id="48930-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48930-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="48930-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48930-106">Parameters</span></span>

<span data-ttu-id="48930-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="48930-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48930-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48930-108">Return value</span></span>

<span data-ttu-id="48930-109">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="48930-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48930-110">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48930-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48930-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48930-111">Requirements</span></span>



| <span data-ttu-id="48930-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48930-112">Requirement</span></span> | <span data-ttu-id="48930-113">Wert</span><span class="sxs-lookup"><span data-stu-id="48930-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48930-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48930-114">Minimum supported client</span></span><br/> | <span data-ttu-id="48930-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="48930-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="48930-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48930-116">Minimum supported server</span></span><br/> | <span data-ttu-id="48930-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48930-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="48930-118">IDL</span><span class="sxs-lookup"><span data-stu-id="48930-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48930-119"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48930-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48930-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48930-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48930-121">**IMF cdmsuspendnotify**</span><span class="sxs-lookup"><span data-stu-id="48930-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




