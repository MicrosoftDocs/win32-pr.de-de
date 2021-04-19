---
description: Die getduecommand-Methode ruft einen Zeiger auf den nächsten Befehl ab, der fällig ist.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Ccmdqueue. getduecommand-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360278"
---
# <a name="ccmdqueuegetduecommand-method"></a><span data-ttu-id="8964c-103">Ccmdqueue. getduecommand-Methode</span><span class="sxs-lookup"><span data-stu-id="8964c-103">CCmdQueue.GetDueCommand method</span></span>

<span data-ttu-id="8964c-104">Die- `GetDueCommand` Methode ruft einen Zeiger auf den nächsten Befehl ab, der fällig ist.</span><span class="sxs-lookup"><span data-stu-id="8964c-104">The `GetDueCommand` method retrieves a pointer to the next command that is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="8964c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8964c-105">Syntax</span></span>


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="8964c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8964c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8964c-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="8964c-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="8964c-108">Adresse eines Zeigers auf den verzögerten Befehl.</span><span class="sxs-lookup"><span data-stu-id="8964c-108">Address of a pointer to the deferred command.</span></span>

</dd> <dt>

<span data-ttu-id="8964c-109">*mstimeout*</span><span class="sxs-lookup"><span data-stu-id="8964c-109">*msTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="8964c-110">Zeitspanne, die gewartet werden soll, bevor das Timeout durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8964c-110">Amount of time to wait before carrying out the time-out.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8964c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8964c-111">Return value</span></span>

<span data-ttu-id="8964c-112">Gibt den \_ Abbruch bei einem Timeout zurück.</span><span class="sxs-lookup"><span data-stu-id="8964c-112">Returns E\_ABORT if a time-out occurs.</span></span> <span data-ttu-id="8964c-113">Gibt \_ bei Erfolg S OK zurück; andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8964c-113">Returns S\_OK if successful; otherwise, returns an error.</span></span> <span data-ttu-id="8964c-114">Gibt ein Objekt zurück, das mit **IUnknown:: adressf** inkrementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8964c-114">Returns an object that has been incremented using **IUnknown::AddRef**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8964c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8964c-115">Remarks</span></span>

<span data-ttu-id="8964c-116">Diese Member-Funktion wird blockiert, bis ein ausstehender Befehl fällig ist.</span><span class="sxs-lookup"><span data-stu-id="8964c-116">This member function blocks until a pending command is due.</span></span> <span data-ttu-id="8964c-117">Die Element Funktionsblöcke für die Zeitspanne (in Millisekunden), die im *mstimeout* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8964c-117">The member function blocks for the amount of time, in milliseconds, specified in the *msTimeout* parameter.</span></span> <span data-ttu-id="8964c-118">Stream-Zeit-Befehle werden nur durch die Member-Funktionen [**ccmdqueue:: Run**](ccmdqueue-run.md) und [**ccmdqueue:: EndRun**](ccmdqueue-endrun.md) verursacht.</span><span class="sxs-lookup"><span data-stu-id="8964c-118">Stream-time commands become due only between the [**CCmdQueue::Run**](ccmdqueue-run.md) and [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) member functions.</span></span> <span data-ttu-id="8964c-119">Der Befehl wird bis zum Ausführen oder Abbrechen in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="8964c-119">The command remains queued until run or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="8964c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8964c-120">Requirements</span></span>



| <span data-ttu-id="8964c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8964c-121">Requirement</span></span> | <span data-ttu-id="8964c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8964c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8964c-123">Header</span><span class="sxs-lookup"><span data-stu-id="8964c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8964c-124"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8964c-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8964c-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8964c-125">Library</span></span><br/> | <dl> <span data-ttu-id="8964c-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8964c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8964c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8964c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8964c-128">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8964c-128">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




