---
description: Ein Rückruf, der den Host von Meldungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixerrorcallback:: messagescallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343937"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span data-ttu-id="ba0c4-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>Ipixerrorcallback:: messagescallback-Methode</span><span class="sxs-lookup"><span data-stu-id="ba0c4-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback::MessagesCallback method</span></span>

<span data-ttu-id="ba0c4-104">Ein Rückruf, der den Host von Meldungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba0c4-104">A callback that notifies the host of messages returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba0c4-105">Syntax</span></span>


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a><span data-ttu-id="ba0c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba0c4-106">Parameters</span></span>

<span data-ttu-id="ba0c4-107">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="ba0c4-107">*count* </span></span>  
<span data-ttu-id="ba0c4-108">Die Anzahl der Meldungen.</span><span class="sxs-lookup"><span data-stu-id="ba0c4-108">The number of messages.</span></span>

<span data-ttu-id="ba0c4-109">*count0- \_ Nachrichten* </span><span class="sxs-lookup"><span data-stu-id="ba0c4-109">*count0\_messages* </span></span>  
<span data-ttu-id="ba0c4-110">Die Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ba0c4-110">The messages.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba0c4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba0c4-111">Return value</span></span>

<span data-ttu-id="ba0c4-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ba0c4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba0c4-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba0c4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0c4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba0c4-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ba0c4-115">Header</span><span class="sxs-lookup"><span data-stu-id="ba0c4-115">Header</span></span></p></td><td><span data-ttu-id="ba0c4-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ba0c4-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ba0c4-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba0c4-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ba0c4-118">**Ipixerrorcallback**</span><span class="sxs-lookup"><span data-stu-id="ba0c4-118">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
