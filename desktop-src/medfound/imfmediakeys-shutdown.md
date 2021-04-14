---
description: 'Weitere Informationen finden Sie unter: IMF Media Keys:: Shutdown-Methode'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'IMF Media Keys:: Shutdown-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351568"
---
# <a name="imfmediakeysshutdown-method"></a><span data-ttu-id="d1fb2-103">IMF Media Keys:: Shutdown-Methode</span><span class="sxs-lookup"><span data-stu-id="d1fb2-103">IMFMediaKeys::Shutdown method</span></span>

## <a name="syntax"></a><span data-ttu-id="d1fb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1fb2-104">Syntax</span></span>


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="d1fb2-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1fb2-105">Parameters</span></span>

<span data-ttu-id="d1fb2-106">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d1fb2-106">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1fb2-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1fb2-107">Return value</span></span>

<span data-ttu-id="d1fb2-108">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d1fb2-108">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1fb2-109">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1fb2-109">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1fb2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1fb2-110">Remarks</span></span>

<span data-ttu-id="d1fb2-111">Das **herunter** fahren sollte von der Anwendung vor der endgültigen Freigabe aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d1fb2-111">**Shutdown** should be called by the application before final release.</span></span> <span data-ttu-id="d1fb2-112">An dieser Stelle wird der CDM-Verweis (Content entschlüsseln Module) und alle anderen Ressourcen veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d1fb2-112">The Content Decryption Module (CDM) reference and any other resources is released at this point.</span></span> <span data-ttu-id="d1fb2-113">Verwandte Sitzungen werden jedoch nicht freigegeben oder geschlossen.</span><span class="sxs-lookup"><span data-stu-id="d1fb2-113">However, related sessions are not freed or closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1fb2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1fb2-114">Requirements</span></span>



| <span data-ttu-id="d1fb2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1fb2-115">Requirement</span></span> | <span data-ttu-id="d1fb2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d1fb2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1fb2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1fb2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1fb2-118">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="d1fb2-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1fb2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1fb2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1fb2-120">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1fb2-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d1fb2-121">IDL</span><span class="sxs-lookup"><span data-stu-id="d1fb2-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1fb2-122"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1fb2-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1fb2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1fb2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fb2-124">**IMF Media Keys**</span><span class="sxs-lookup"><span data-stu-id="d1fb2-124">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




